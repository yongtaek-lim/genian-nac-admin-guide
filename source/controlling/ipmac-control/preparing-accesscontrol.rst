Preparing Access Control using IPAM
===================================

You can enable Enforcement by changing Denied by IPAM default policy, and change each individual Sensors default policies

To Enable “Denied by IPAM” Policy
---------------------------------

By default, the “**Denied by IPAM**” enforcement policy is disabled. Before controlling nodes using the Policy, the enforcement policy for  “**Denied by IPAM**” must be enabled.

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Click **IPAM Denied** name in the Enforcement Policy window
#. Find **General > Application Mode** section to **Enable**
#. Click **Update**
#. Click **Apply** in top right corner

To Change IPAM Default Policy
-----------------------------

Each sensor has a default IPAM Policy. When a new node is detected by the sensor, or if an IP or MAC Address is showing on the network for the first time, the default policy is automatically applied.

- **Deny MAC**: Deny a MAC Address
- **Deny IP**: Deny an IP Address
- **Deny IP/MAC**: Deny an IP and MAC Address
- **Allow**: Allow an IP and MAC (default)
- **Enable Change Prevention**: Enable IP Change Prevention for a node’s IP/MAC
- **Enable Conflict Prevention**: Enable IP conflict Prevention for a node’s IP/MAC

To Change Sensors IPAM Default Policy
-------------------------------------

The Default Policy can be changed on each sensor’s settings

#. Go to **System** in the top panel
#. Go to **System > Sensor** in the left System Management panel
#. Click the desired sensor’s **IP Address**
#. Click the **Settings** tab and click **Sensor Settings**
#. Find **IPAM Policy** section, change **IPAM Policy** for **New Node** accordingly
#. Click **Update**
