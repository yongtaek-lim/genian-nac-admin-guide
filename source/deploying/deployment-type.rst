Deployment Models
=================

Compare Deployment Methods
--------------------------

Genian NAC support multi-layered deployment methods include:

  - Layer 2 Sensor/Enforcer (*Mandatory*)
  - SNMP/CLI
  - Port Mirroring (SPAN)
  - 802.1x
  - Agent

The table below compares the advantages and disadvantages of each method. 

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Topic
     - Layer 2 Sensor/Enforcer
     - SNMP/CLI
     - Port Mirroring (SPAN)
     - 802.1x
     - Agent
   * - **Pre Connect Control**
     - | Yes 
     - | Yes
     - | No
     - | Yes
     - | No
   * - **Post Connect Control**
     - | Yes
     - | Change VLAN/ACL/Shutdown
     - | TCP Only
     - | CoA* required
     - | Yes
   * - **Layer 3 Access Control**
     - | RBAC
     - | Switch Port ACL
     - | RBAC
     - | Switch  Port ACL
     - | OS Firewall
   * - **Additional Hardware**
     - | Network Sensor       
     - | Replace to Managed Switch
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
   * - **Network Config Change**
     - | Config trunk port (optional)
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
     - | SNMP MIB/CLI command
       | support issue
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
   * - **Recommended**
     - | Basic monitoring and control
     - | For extended information
       | and port control
     - | Not recommended
     - | For wireless network
     - | For extended information
       | and enforce compliance


*CoA\*: Change of Authorization, RFC 5176 - Dynamic Authorization Extensions to RADIUS*

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

