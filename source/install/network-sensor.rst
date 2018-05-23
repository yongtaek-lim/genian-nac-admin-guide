Installing Network Sensor
=========================

You can install Network Sensor on a Physical Machine or Virtual Machine

#. Create an installation media

   - Download the Policy Server ISO file from the www.genians.com
   - Create a CD-ROM or bootable USB flash drive

#. Check out your network connection

   - Connect at least one wired network cable to the machines network interface
   - Genian NAC supports access port and trunk (802.1q) port connection within a switch
   - A Static IP is required for the management interface
   - Network interface type: Bridged (**Virtual Machine**)

#. Boot up your machine

   - Plug the CD-ROM or bootable USB flash drive into your physical machine
   - Change the boot sequence to boot from the CD-ROM or USB drive
   - Boot it up! (* This process will copy the image from the CD-ROM or bootable USB flash drive to your physical machine.)
   - Press enter to start installation
   - Install a Genian NAC Network Sensor

     - Type "i" to proceed
     - Type "e" to exit

#. Reboot your system

   - Remove the installation media (e.g. USB)
   - Press Enter to reboot

#. Create admin account

#. Set up a system time

   - Continent, City
   - NTP Server (* Leave it blank if you don’t have one)

#. Configure Network Management Interface

   - In case the interface eth0 is connected to 802.1Q trunk port  up to 182 VLANs
   - Enter VLAN IDs (*Concatenated by comma*)
   - Enter VLAN ID for management interface
   - IP Address
   - Netmask
   - Default Gateway
   - DNS IP addresses (*concatenated by comma*)

#. Verify all information

#. Type “y” to start

#. In case the interface eth0 is not connected to 802.1Q trunk port (a single network)

#. Enter Network Interface information

   - IP address
   - Netmask
   - Default Gateway
   - DNS IP addresses (*concatenated by comma*)

#. Verify all information

#. Type "y" to start
