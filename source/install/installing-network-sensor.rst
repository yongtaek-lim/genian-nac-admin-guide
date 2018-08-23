Installing Network Sensor
=========================
    
Prepare Hardware
----------------

You can install Network Sensor on a physical machine or virtual machine. Please refer `minimum specification`_.

**Physical Machine**
    You can use generic intel server like HP, Dell or Mini PC for testing and small deployment. 
    If you have any hardware comparability issue, please `contact us`_
    
**Virtual Machine**
    You can install Network Sensor on virtual machine. We support various hypervisor 

Prepare Network Connection
--------------------------

Genian NAC requires a network connection with at least one static IP address. 
You can use an 802.1Q trunk port to manage multiple VLANs on a single network connection.
If you are using a virtual machine, be sure to select the network interface type in **Bridge** mode.

Download Software
-----------------

   -  Download the Policy Server ISO file from the `download page`_
   -  Create a CD-ROM or :doc:`/install/bootable-usbdrive` for physical machine installation

Installing Network Sensor
-------------------------

#. Boot up your machine

    * Plug the CD-ROM or bootable USB flash drive into your physical machine
    * Change the boot sequence to boot from the CD-ROM or USB drive
    * On virtual machine, select ISO file for installation media

#. Type “2” for **Genian NAC Sensor**
#. Type “i” to proceed
#. Reboot your system

    * Remove the installation media (*e.g. USB*)
    * Press Enter to reboot

Initial Configuration
---------------------

#. Create admin account for SSH connection

    * Enter superadmin account name. (default is *admin*)
    * Enter superadmin password
    
#. Set up a system time zone and NTP server

    * Enter number of your continent and city
    * Enter NTP server IP or FQDN (default is *pool.ntp.org*)

#. Select connection type

    * In case the interface eth0 is connected access port (regular port)
    
        * Type "n"
        
    * In case the interface eth0 is connected to 802.1Q trunk port

        * Type "y"
        * Enter VLAN IDs for service (*Concatenated by comma or A-B for range. e.g: 10,20-30*)
        * Enter VLAN ID for management interface

#. Network configuration

    * Enter IP address
    * Enter netmask
    * Enter default gateway
    * Enter DNS IP addresses (*Concatenated by comma*)
    
#. Enter Policy Server IP or FQDN.
    
#. Verify all information

    * Everythings correct. Type “y” to start
    * Something wrong. Type "n" to restart configuration
    
#. If the connection to the policy server is successful, you can check the newly added network sensor in **System> System** menu of the management UI.

.. _minimum specification: https://www.genians.com/download/
.. _contact us: https://www.genians.com/hello/
.. _download page: https://www.genians.com/download/
