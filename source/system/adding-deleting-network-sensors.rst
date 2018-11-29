Adding And Deleting Network Sensors
===================================

As your network changes, you may add or delete VLANs in your current network configuration. 
You can add Sensors to manage these newly created VLANs by adding additional interfaces in the 
Network Sensor CLI. If you add additional remote locations you can add Network Sensor Appliances 
to the sites to have these locations managed through Genian NAC.

Add Additional Network Sensors (VLANs)
--------------------------------------

(*Network Sensors cannot be added through UI, they must be configured through CLI by adding sub-interfaces 
to the existing eth0 or eth1 interface.*)

#. Connect through **SSH client** to Network Sensor :doc:`connect-cli`
#. Enter global configuration mode by typing **configure terminal**
#. Enter the following commands below for each Network Sensor to be added:
 
   -  interface eth0 vlan "**All VLAN IDs** separated by comma and hyphen" (*e.g. interface eth0 vlan 1,10-15*)
   -  interface eth0.x address 10.1.x.5 255.255.255.0

#. Type **exit**

Delete A Specific VLAN Network Sensor
-------------------------------------

(*This deletes a single VLAN Network Sensor and all Nodes and Node information*)

#. Connect through **SSH client** to Network Sensor :doc:`connect-cli`
#. Enter global configuration mode by typing **configure terminal**
#. Enter the following commands below for each Network Sensor (VLAN) to be removed:

   -  interface eth0 vlan "**All VLAN IDs** separated by comma and hyphen" (*e.g. interface eth0 vlan 1,10-15*)
   -  no interface eth0.x address 10.1.x.5 255.255.255.0

#. Exit from **CLI**
#. Go to **System** in the top panel
#. Go to **System > Sensor** in the System Management panel
#. Find and click on the **IP Address** of desired Network Sensor
#. Find and click **Delete** in General tab
#. click **OK** to confirm

Add Network Sensor Hardware
---------------------------

If you have added a new remote location, here are the steps to adding an additional Network 
Sensor hardware to your Policy Server.

#. Go to :doc:`/install/installing-network-sensor` (*During the Installation of Network Sensor a question will be presented to point to a node-server host*)
#. For **node-server host** enter **IP Address (On-Premise)** or use **FQDN (Cloud)** (*e.g. node-server host 192.168.50.50 or node-server host somename.domain.net*)
#. Deploy **Network Sensor** onto Network :doc:`/deploying/deployment-type`
#. Should see **Network Sensor** in UI under **System > Sensor and Management > Node**

Delete A Network Sensor System
------------------------------

(*This deletes a Network Sensor System and all VLANs(Up to 128) with Nodes and Node information for all associated networks*)

#. Disconnect **Network Sensor** from the network and power down
#. Access **Policy Server UI** to delete Network Sensor
#. Go to **System** in the top panel
#. Go to **System > System** in the System Management panel
#. Find and click on the **Checkbox** of desired Network Sensor
#. Go to **Tasks > Delete System**
#. click **OK** to confirm
