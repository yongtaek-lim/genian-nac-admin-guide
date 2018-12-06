Deployment Models
=================

Compare Deployment Methods
--------------------------

The deployment method describes how Genian NAC collects network information and controls the network access of devices. 

Genian NAC support multi-layered deployment methods include:

  - Layer 2 Sensor/Enforcer (*Mandatory*)
  - SNMP/CLI
  - Port Mirroring (SPAN)
  - 802.1x
  - Agent

Of these, Layer 2 Networks Sensors must be installed with Policy Server when deployed as an integral component of Genian NAC.
Other deployment methods can be optionally applied.

The table below compares the advantages and disadvantages of the functional point of view.

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Topic
     - Layer 2 Sensor/Enforcer
     - SNMP/CLI
     - Port Mirroring (SPAN)
     - 802.1x
     - Agent
   * - **Layer 2 Access Control**
     - | Yes 
     - | Yes
     - | No
     - | Yes
     - | No
   * - **Layer 3 Access Control**
     - | RBAC
     - | Switch Port ACL
     - | RBAC
     - | Switch  Port ACL
     - | OS Firewall
   * - **Post Connect Control**
     - | Yes
     - | VLAN/ACL/Shutdown
     - | TCP Only
     - | CoA* required
     - | Yes
   * - **Additional Hardware**
     - | Network Sensor       
     - | Managed Switches
     - | Full traffic capable Device,
       | Tap Device,
       | SSL Decryption Device
     - | 802.1x supported Switches
     - | No
   * - **Endpoint Dependency**
     - | No
     - | No
     - | No
     - | 802.1x Supplicant
     - | Agent required
   * - **Secure WiFi**
     - | No
     - | No
     - | No
     - | WPA2-Enterprise,
       | EAP-TLS, EAP-TTLS
     - | Yes
   * - | **WiFi Security**
       | - Rogue AP Detect
       | - Connection Monitor
     - | Yes
     - | Through AP or Controller
     - | No
     - | No
     - | Yes
   * - **Layer 2 Security**
     - | Detect MAC Spoofing,
       | Detect Rogue DHCP,
       | Managing IP Conflict
     - | No
     - | No
     - | No
     - | No

*CoA\*: Change of Authorization, RFC 5176 - Dynamic Authorization Extensions to RADIUS*

To build network access control effectively and quickly, it is necessary to use a variety of deployment methods that
are appropriate for network characteristics and security requirements.

The table below compares the advantages and disadvantages of the deployment and management point of view.

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Topic
     - Layer 2 Sensor/Enforcer
     - SNMP/CLI
     - Port Mirroring (SPAN)
     - 802.1x
     - Agent
   * - **Network Config Change**
     - | Trunk port (optional)
     - | Switch Config,
       | VLAN/ACL
     - | Tap Device,
       | SPAN Port
     - | Switch Config,
       | VLAN/ACL,
       | Endpoint Config
     - | No
   * - **Compatibility Issue**
     - | No
     - | Vendor-dependent
       | SNMP MIB/CLI
     - | No
     - | RADIUS Vendor Attribute,
       | non-802.1x capable Device
       | (*Poor wired device support*)
     - | OS Type/Version
   * - **Easy of Deployment**
     - | Easy
     - | Difficult
     - | Intermediate
     - | Very Difficult
     - | Intermediate
   * - | **Phased Deployment**
       | - Discover First
       | - Control Later
     - | Yes
     - | Yes
     - | Yes
     - | Must be controlled from
       | the start of deployment
     - | Yes
   * - **Single point of Failure**
     - | No
     - | Yes
     - | Yes
     - | Yes
     - | No
   * - **Vendor Lock-in**
     - | No
     - | Intermediate
     - | No
     - | High
     - | Intermediate
   * - **Recommended for**
     - | Essential Discovery
       | and Control
     - | Extended information
       | and port control
     - | 
     - | Wireless network
     - | Extended information
       | and enforce compliance

Policy Server Deployment Models
-------------------------------

On-Premises
'''''''''''

**Policy Server** and **Network Sensor** can be deployed one of two ways

   -  Policy Server/Network Sensor combined
   -  Policy Server and Network Sensor separated
   
The switch port can be a standard connection or can be a trunked port for up to 128 VLANs. If your location has more than 128 VLANs then a second Network Sensor would be required
(*If you have 2 Network Sensors on the same network or overlapping networks in an 802.1q environment you will have duplicate nodes. There is no harm in having duplicated nodes, it is just something to be aware of.*)

Policy Server and Network Sensor Combined

.. image:: /images/Deploying-PolicyServer-NetworkSensor-Combined.png
   :width: 600px

Policy Server and Network Sensor Separated

.. image:: /images/Deploying-PolicyServer-NetworkSensor.png
   :width: 600px

Cloud-Managed
'''''''''''''

**Policy Server** can be deployed in the Cloud, while **Network Sensors** can be deployed by connecting them to an Edge Switch at your Remote Site locations.  The Edge Switch ports can be a standard connection or can be trunked ports for up to 128 VLANs. If your location has more then 128 VLANs then a second **Network Sensor** would be required

.. image:: /images/Deploying-PolicyServer-NetworkSensor-Cloud.png
   :width: 600px

