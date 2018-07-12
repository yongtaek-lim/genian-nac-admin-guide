Adding And Deleting Network Sensors
===================================

As your network changes, you may add or delete VLANs in your current network configuration. 
You can add Sensors to manage these newly created VLANs by adding additional interfaces in the 
Network Sensor CLI. If you add additional remote locations you can add Network Sensor Appliances 
to the sites to have these locations managed through Genian NAC.

To Add Additional Network Sensors (VLANs)
-----------------------------------------

(*Network Sensors cannot be added through UI, they must be configured through CLI by adding sub-interfaces 
to the existing eth0 or eth1 interface.*)

#. Connect through **SSH client** to Network Sensor `Connecting To Command Line Interface`_
#. Enter global configuration mode by typing **configure terminal**
#. Enter the following commands below for each Network Sensor to be added:
 
   -  interface eth0 vlan "Include all VLANs and add in the new VLAN ID" (*If you do not iunclude* **ALL VLAN IDs** *then the one left out will be deleted*)
   -  interface eth0.x address 10.1.x.5 255.255.255.0

#. exit

(*Commands are instantly written so there is no need to do “write” or “copy run start” commands*)

To Delete A Specific VLAN Network Sensor
----------------------------------------

(*This deletes a single VLAN Network Sensor and all Nodes and Node information*)

#. Connect through **SSH client** to Network Sensor `Connecting To Command Line Interface`_
#. Enter global configuration mode by typing **configure terminal**
#. Enter the following commands below for each Network Sensor (VLAN) to be removed:

   -  interface eth0 vlan 1,10,15 "Include all VLANs except the one you want to delete" (*If you do not iunclude* **ALL VLAN IDs** *then the one left out will be deleted*)
   -  no interface eth0.x address 10.1.x.5 255.255.255.0

#. Exit from **CLI**
#. Go to **System** in the top panel
#. Go to **System > Sensor** in the System Management panel
#. Find and click on the **IP Address** of desired Network Sensor
#. Find and click **Delete** in General tab
#. click **OK** to confirm

To Add Network Sensor Hardware At New Remote Site
-------------------------------------------------

If you have added a new remote location, here are the steps to adding an additional Network 
Sensor hardware to your Policy Server.

#. Go to `Installing Network Sensor`_ (*During the Installation of Network Sensor a question will be presented to point to a node-server host*)
#. For **node-server host** enter **IP Address (On-Premise)** or use **FQDN (Cloud)** (*e.g. node-server host 192.168.50.50 or node-server host somename.domain.net*)
#. `Deploy Network Sensor onto Network`_
#. Should see **Network Sensor** in UI under **System > Sensor and Management > Node**

To Delete A Network Sensor System
---------------------------------

(*This deletes a Network Sensor System and all VLANs(Up to 128) with Nodes and Node information for all associated networks*)

#. Disconnect **Network Sensor** from the network and power down
#. Access **Policy Server UI** to delete Network Sensor
#. Go to **System** in the top panel
#. Go to **System > System** in the System Management panel
#. Find and click on the **Checkbox** of desired Network Sensor
#. Go to **Tasks > Delete System**
#. click **OK** to confirm

.. _Installing Network Sensor: https://www.genians.com/docs/administrators-guide/?section=installing-network-sensor
.. _Deploy Network Sensor onto Network: https://www.genians.com/docs/administrators-guide/?section=deploying-policy-server
.. _Connecting To Command Line Interface: https://www.genians.com/docs/administrators-guide/?section=connecting-command-line-interface
