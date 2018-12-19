Rogue Gateway
=============

A Genian Agent can immediately detect a rogue gateway configuration in a variety of ways. 
If a gateway address (or default gateway) configured on a Node is not on the trusted network, Genians designates the Node as a critical one. 
This may go with not only an Agent Control option in Definition configuration settings alone but also a Plugin Agent Action, Control Interface, which broadens Agent's capabilities. 
(*Refer to Controlling Endpoints » Controlling Windows » Controlling Network Interface.*)

For running an Agent Action to control an interface, please see :doc:`/endpoints/network-interface` 


Step 1. Configure Settings for Rogue Gateway in Anomaly Definition
------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Rogue Gateway**
#. Find **Anomaly Event** section to configure more options
#. For **Trusted Network Scope** (*An option may be configurable in Policy > Object > Network.*)
#. For **Sensor Network as Trusted** (*This prevents from not being on the trusted network if a Sensor changes its management scope.*)
#. For **Agent Control** select **Yes** to configure more options and you may specify the followings:

   - **Response:** Disabling Device or Generating Logs
   - **Interface Disabled Notification:** Yes or No
   - **External Device Exceptions:** optional setting to specify the device to be an exception to this Anomaly (*The name must be the exact match, therefore, you had better configure Interface Type Exception instead*)  
   - **Interface Type Exception:** Wired, Wireless or Virtual

#. Click **Update**

Step 2. Create Status Group For Rogue Gateway Configured
--------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Rogue Gateway Configured
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** Rogue Gateway

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect Rogue Gateway Through Node Policy
------------------------------------------------

You may assign the Status Group of Spoofed ARP Sent you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **Rogue Gateway** pre-configured in Step 1. 
The anomaly, **Rogue Gateway**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block Rogue Gateway Through Enforcement Policy
------------------------------------------------------

You may assign the Status Group of Rogue Gateway Configured you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **Rogue Gateway** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.