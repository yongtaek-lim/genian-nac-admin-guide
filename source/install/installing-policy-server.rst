Installing Policy Server
========================

You can install **Policy Server** on a **Physical Machine** or **Virtual Machine**

#. Create an installation media

   -  Download the Policy Server ISO file from the www.genians.com `download page`_

   -  Create a CD-ROM or `bootable USB flash drive`_

#. Check out your network connection

   -  Connect at least one wired network cable to the machines network interface

   -  Genian NAC supports access port and trunk (802.1q) port connection within a switch

   -  A Static IP is required for the management interface

   -  Network interface type: **Bridged** (*Virtual Machine*)

#. Boot up your machine

  1. Plug the CD-ROM or bootable USB flash drive into your physical machine
  2. Change the boot sequence to boot from the CD-ROM or USB drive
  3. Boot it up! (*This process will copy the image from the CD-ROM or bootable USB flash drive to your physical machine.*)

#. Select a Product

   -  Type “1” for Genian NAC Policy Server + Sensor

#. Install a Product

   -  Type “i” to proceed

   -  Type “e” to exit

#. Reboot your system

   -  Remove the installation media (*e.g. USB*)

   -  Press Enter to reboot

#. Create admin account

#. Set up a system time

   -  Continent, City

   -  NTP Server (*Leave it blank if you don’t have one*)

#. Configure Network Management Interface

   -  In case the interface eth0 is connected to 802.1Q trunk port up to 182 VLANs

    1. Enter VLAN IDs (*Concatenated by comma*)

    2. Enter VLAN ID for management interface

      -  IP Address

      -  Netmask

      -  Default Gateway

      -  DNS IP addresses (*Concatenated by comma*)

    3. Verify all information

    4. Type “y” to start

   -  In case the interface eth0 is not connected to 802.1Q trunk port (*a single network*)

    1. Enter Network Interface information

      -  IP address

      -  Netmask

      -  Default Gateway

      -  DNS IP addresses (*concatenated by comma*)

    2. Verify all information

    3. Type “y” to start

#. Login to Genian NAC web console

.. _download page: https://www.genians.com/download#now
.. _bootable USB flash drive: https://www.genians.com/knows/create-a-bootable-usb-drive/

.. toctree::
   :maxdepth: 2

   gui
   ssh
   license
   high-availability
