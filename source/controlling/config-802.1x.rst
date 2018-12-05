Configuring 802.1X
==================

What is 802.1X
--------------

IEEE 802.1X is an IEEE Standard for port-based Network Access Control (PNAC).
It is part of the IEEE 802.1 group of networking protocols.
It provides an authentication mechanism to devices wishing to attach to a LAN or WLAN.

802.1X authentication involves three parties: a supplicant, an authenticator, and an authentication server.

The supplicant is a client device (such as a laptop) that wishes to attach to the LAN/WLAN.
The term 'supplicant' is also used interchangeably to refer to the software running on the client that provides credentials to the authenticator.

The authenticator is a network device, such as an Ethernet switch or wireless access point.
The authenticator acts like a security guard to a protected network. The supplicant is not allowed access
through the authenticator to the protected side of the network until the supplicant’s identity has been validated and authorized.

With 802.1X port-based authentication, the supplicant provides credentials, such as username/password or digital certificate,
to the authenticator, and the authenticator forwards the credentials to the authentication server for verification.
If the authentication server determines the credentials are valid, the supplicant (client device) is allowed to access resources
located on the protected side of the network.

Authentication
--------------

Genian NAC provides a built-in RADIUS Authentication server to provide 802.1X user authentication.
To do this, the following settings are typically required on the authenticator (ie, wirelesss access point).

- Set the security setting of each access port or SSID to 802.1X
- RADIUS server settings to forward user authentication requests received from Supplicant

To run Genian NAC's RADIUS server, the administrator must first activate the server through configuration
and register the user in the local user database for authentication or integrate with an external user directory (eg LDAP).

Enable Built-In RADIUS Server
`````````````````````````````

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left panel

Under **Authentication Server**

#. For **Shared Secret Key**, enter the pre-shared secret key for RADIUS client(authenticator) authentication.
#. For **RADIUS Client IP**, enter the IP address or addresses to be allowed as Clients separated by new line.
#. For **Server Port**, enter the RADIUS authentication port number (*Default is 1812*)
#. For **EAP Authentication**, select **On**
#. For **Generating Accounting**, select **On** if RADIUS client(authenticator) not support generating RADIUS accounting packet
#. Click **Update**

MAC Authentication Bypass (MAB)
```````````````````````````````
 
Not all devices support 802.1X authentication. Examples include network printers, Ethernet-based electronics like environmental sensors,
cameras, and wireless phones. For those devices to be used in a protected network environment, alternative mechanisms must be provided to authenticate them.

When MAB is configured on a port, that port will first try to check if the connected device is 802.1X compliant, and if no reaction is received from the connected device,
it will try to authenticate with the RADIUS server using the connected device's MAC address as username and password.

Genian NAC can select the MAC address to be allowed through the Node Group. If the MAC that is requested to be authenticated is exists in the Node Group,
the authentication is allowed; otherwise, the authentication is denied.

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left panel

Under **Authentication Server**

#. For **MAC Authentication**, select **On** for enable MAC Authentication bypass (MAB)
#. For **Node Group**, select Node Group for allow MAC authentication
#. Click **Update**

Authorization
-------------

If you want to control the network connection according to the role for the device that has been granted user authentication and is allowed to access the network,
you can control it by assigning another VLAN at 802.1X authentication. To accomplish this, the switch or access point must support the RADIUS Tunnel-Private-Group-ID attribute.

Enable Quarantine VLAN
``````````````````````

Genian NAC provides the ability to specify which VLANs to assign to devices belonging to a specific Node Group for non compliance compliant devices.

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left panel

Under **Authentication Server**

#. For **EAP Authentication**, select **On**
#. For **Quarantine VLAN**, select **On**
#. For **VLAN Number**, enter VLAN ID for non compliant device
#. For **Node Group**, select Node Group for non compliant devices
#. For **VLAN for New Node**, select **On** to assign a quarantine VLAN for all new nodes
#. Click **Update**

Enable CoA (Change of Authorization)
````````````````````````````````````

If device violates compliance during network use, it should be changed back to the isolated VLAN.
This is provided through a standard called CoA (Change of Authorization, RFC 5176 - Dynamic Authorization Extensions to RADIUS standard).

The CoA disconnects the current connection to the device for which the enforcement policy has changed.
The disconnected device will attempt to reconnect and then move to the isolated VLAN through VLAN assignment.

#. Go to **Policy** in the top panel
#. Go to **Policy > Enforcement Policy** in the left panel
#. Click the name of the Enforcement Policy you want to disconnect

Under **Enforcement Options > RADIUS Control**

#. For **RADIUS CoA**, select **On**
#. For **CoA Commands**, select **Terminate Session** for standard attribute or select other VSA (Vendor Specific Attribute)
#. For **Vendor-Specific-Attribute**, enter VSA values (eg Nas-filter-Rule='permit in tcp from any to any 23')

Under **Authentication Server**