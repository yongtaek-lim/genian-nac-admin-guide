Rogue Gateway Configured
=========================

A Genian Agent can immediately detect a rogue gateway configuration in a variety of ways. 
If a gateway address (or default gateway) configured on a Node is not on the trusted network, Genians designates the Node as a critical one. 
This may go with not only an Agent Control option in Definition configuration settings alone but also a Plugin Agent Action, Control Interface, which broadens Agent's capabilities.
(*Refer to Controlling Endpoints » Controlling Windows » Controlling Network Interface.)
.. toctree::
   :maxdepth: 1

   controlling-windows/network-interface


Step 1. Configure Anomaly Event Options for Rogue Gateway in Anomaly Definition
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly** in the left Policy panel
#. Click **Rogue Gateway**
#. Find **Anomaly Event** section
#. Specify **Trusted Network Scope** (*An option may be configurable in Policy > Object > Network.)
#. Specify **Sensor Network as Trusted** (*This prevents from not being on the trusted network if a Sensor changes.)
#. Select **Yes** to configure more options for Agent Control
#. For **Agent Control** you may specify the followings:

   - Response, you can choose either "Disabling Device" or "Generating Logs"
   - Interface Disabled Notification
   - Device Exception, you can enter a device name (*The name must be the exact match, therefore, you may also configure Interface Type Exception instead)
   (*You may refer to Device Manager in Widnows and choose one of the device you would like to exclude from Disabling Device.)
   - Interface Type Exception, you can choose one of No Exceptions, Wired, Wireless or Virtual
#. Click **Update**

Step 2. Create Status Group For Rogue Gateway Configured
----------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "Rogue Gateway Configured", Status "Enabled"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **Rogue Gateway**

#. Click **Update**
   
Step 3. Create Node Policy For Rogue Gateway
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "Rogue Gateway Configured", Status "Enabled"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **Rogue Gateway Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** (*Or you may select configured Agent Action **Control Network Interface**)
#. On **Anomaly** tab, select **Rogue Gateway**
#. Click **Finish**

