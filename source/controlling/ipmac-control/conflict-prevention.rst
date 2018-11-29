Configuring IP Conflict Prevention
==================================

You can prevent users from changing their IP Address. Changing an IP can lead to conflicts or compromising issues where users can gain privileges they were not intended to have. For instance, an Administrator could have a designated IP Address set up to allow internet access, while all others are blocked. If an employee is able to change their IP to that designated address, then that employee will gain internet access when they are not allowed to.

How IP Change Prevention Works
------------------------------

The Sensor watches and analyzes packets that are being sent from each device. When a new node is detected, the Sensor sends a gratuitous ARP request. If a machine receives an ARP request containing a source IP that matches its own, then it knows there is an IP conflict.

To Enable IP Conflict Prevention
--------------------------------

#. Go to **Management > Node** in the top panel
#. Click on the desired **IP** or **MAC Address**
#. Click **IPAM** tab
#. Find **IP Policy** section, click the **circle** next to **Allow IP – Enable Conflict Prevention**
#. Find **Specify MAC Addresses** section. Locate desired **MAC Address** to Add. Click **Add MAC**
#. Click **Update**

To Disable IP Conflict Prevention
---------------------------------

#. Go to **Management > Node** in the top panel
#. Click on the desired **IP** or **MAC Address**
#. Click **IPAM** tab
#. Find **IP Policy** section, click the **circle** next to **Allow IP – Disable Conflict Prevention**
#. Click **Update**
