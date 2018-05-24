To Change The Interface IP Address
==================================

You can edit and change the appliance IP Address of any interface through the CLI

To Change The Interface IP Address
----------------------------------

#. Login to the CLI
#. Enter Config mode
#. Enter “interface eth0 address (IP Address)(Subnet Mask)” as seen below

.. code:: bash

    genian# conf t
    genian(config)# interface eth0 address 192.168.50.43 255.255.255.0
    Stopping Service...done
    genian(config)# exit
    
To Confirm Interface IP Address Change
--------------------------------------

#. Enter "show configuration | grep interface eth0" as seen below

.. code:: bash

    genian# show configuration | grep interface eth0
    interface eth0 address 192.168.50.43 255.255.255.0
    interface eth0 gateway 192.168.50.1
    interface eth0 management-server enable
    interface eth0 node-server enable
    interface eth0 radius-server enable
    genian# exit
