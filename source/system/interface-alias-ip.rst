Add Alias IP to Sensor Interface
================================

If there is more than one logical subnet in a broadcast domain (VLAN), you need to configure Alias IP on the sensor's interface so that it can be recognized.

Add Alias IP
---------------

#. Go to **System** in top panel
#. Go to **System > System** in the left panel
#. Click desired Network Sensor IP
#. Click **IP Address** tab
#. Click desired interface name for adding alias IP
#. Click **Add** button beside of Sensor IP
#. Enter following information for alias IP

   - IP Address: Management IP for sensor
   - Subnet Mask
   - Gateway
   - IP Pool: let this value blank if you want manage whole subnet

#. Click **Update**

Delete Alias IP
------------------

#. Go to **System** in top panel
#. Go to **System > System** in the left panel
#. Click desired Network Sensor IP
#. Click **IP Address** tab
#. Click desired interface name for adding alias IP
#. Click **Delete** link on desired alias IP under **Sensor IP**
