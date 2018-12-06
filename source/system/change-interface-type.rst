Change Network Sensor Interface Type
====================================

Changing the network configuration may change the interface type of the network sensor from the access port to the trunk port, or vice versa.
This chapter describes how to change the sensor interface type.

Access Port to Trunk Port
-------------------------

.. note:: This example assumes that the physical interface is eth0.


Check existing interface configuration and save existing config. If there are any settings other than IP or Gateway on the interface you want to change, you must transfer the settings to the new interface.

.. code:: bash

    genian# show config
    ...
    interface eth0 address 192.168.50.22 255.255.255.0
    interface eth0 gateway 192.168.50.1
    interface eth0 management-server enable
    interface eth0 node-server enable
    interface eth0 radius-server enable
    ...

Create VLAN interface on physical interface

.. code:: bash

    genian(config)# interface eth0 vlan 10,20,30-35                  // Replace by your VLAN IDs separated by comma or hyphen

If your trunk port has a native VLAN, eth0 will be the native VLAN. any other VLAN interface name will be **ethX.VLANID**. If you don't have the native VLAN,
You should delete eth0 interface settings. 

.. code:: bash

    genian(config)# no interface eth0 address X.X.X.X
    genian(config)# no interface eth0 gateway X.X.X.X
    genian(config)# no interface eth0 management-server enable       // Optional
    genian(config)# no interface eth0 node-server enable             // Optional
    genian(config)# no interface eth0 radius-server enable           // Optional

Setup static IP of VLAN interface and Gateway

.. code-block:: bash

    genian(config)# interface eth0.10 address X.X.X.X
    genian(config)# interface eth0.10 gateway X.X.X.X
    
Or setup DHCP (In case not using static IP)

.. code:: bash

    genian(config)# interface eth0.10 dhcp enable

Restore other config for Management interface (Optional)

.. code:: bash

    genian(config)# interface eth0 management-server enable
    genian(config)# interface eth0 node-server enable
    genian(config)# interface eth0 radius-server enable

**Make sure all VLAN interface properly setup ether static IP or DHCP.**

To configure running network sensor on VLAN interface:

#. Login to administrator Web UI and go to **System** menu
#. Click Network Sensor IP and go to **Sensor** tab
#. Click interface name
#. Change **Sensor Mode** from **None** to **Host**
#. Click **Update** on bottom

When an interface is removed from the CLI settings, any sensors or nodes that were registered in the management console are not automatically deleted.
To delete a sensor that no longer exists and the node it detects, follow these steps:

#. Goto **System** menu
#. Select **System > Sensor** on left panel
#. Click **IP** on desired sensor (You can identified by interface name on hostname column)
#. Click **Delete** on bottom

Trunk Port to Access Port
-------------------------

Delete VLAN

.. code:: bash

    genian(config)# no interface eth0 vlan 10,20,30-35               // Replace by your VLAN IDs separated by comma or hypen

Delete all VLAN interface settings

.. code:: bash

    genian(config)# interface eth0.X address X.X.X.X
    genian(config)# interface eth0.X gateway X.X.X.X

Setup eth0 address, gateway and other settings