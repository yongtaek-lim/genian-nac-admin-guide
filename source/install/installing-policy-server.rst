Installing Policy Server
========================

Choose Deployment Type
----------------------

Policy Server can be installed in two different ways.

**Policy Server Only**
    System only work for Policy Server functionality. In general, on a large network, separate the policy server and network sensor 
    for performance and reliability. At least two systems are required for this deployment type.

**Policy Server + Network Sensor (All-in-One)**
    In a small network, a system can function as a policy server and network sensor.
    
Prepare Hardware
----------------

You can install Policy Server on a physical machine or virtual machine. Please refer `minimum specification`_.

**Physical Machine**
    You can use generic intel server like HP, Dell or Mini PC for testing and small deployment. 
    If you have any hardware comparability issue, please `contact us`_
    
**Virtual Machine**
    You can install Policy Server on virtual machine. We support various hypervisor 

Prepare Network Connection
--------------------------

Genian NAC requires a network connection with at least one static IP address. 
If you configure the All-in-One to use the network sensor function, You can use an 802.1Q trunk port to manage multiple VLANs on a single network connection.
If you are using a virtual machine, be sure to select the network interface type in **Bridge** mode.

Download Software
-----------------

Download the Policy Server ISO file from the `download page`_
and create a CD-ROM or bootable USB for physical machine installation
   
.. toctree::
   :maxdepth: 1

   bootable-usbdrive

Installing Policy Server
------------------------

#. Boot up your machine

    * Plug the CD-ROM or bootable USB flash drive into your physical machine
    * Change the boot sequence to boot from the CD-ROM or USB drive
    * On virtual machine, select ISO file for installation media

#. Type “1” for **Genian NAC Policy Server + Sensor**
#. Type “i” to proceed
#. Reboot your system

    * Remove the installation media (*e.g. USB*)
    * Press Enter to reboot

Initial Configuration
---------------------

#. Create admin account for Web UI and SSH connection

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

#. Verify all information

    * Everythings correct. Type “y” to start
    * Something wrong. Type "n" to restart configuration

#. Login to Genian NAC management UI. :doc:`gui`

.. _minimum specification: https://www.genians.com/download/
.. _contact us: https://www.genians.com/hello/
.. _download page: https://www.genians.com/download/
