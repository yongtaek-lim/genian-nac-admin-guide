Multi-Homed / Ad hoc Network
============================

A Genian Agent can immediately detect a multi-homed configuration and Ad hoc network connection in a variety of ways.
If a computer having more than one IP address configured connects to more than one network and one of them is not on the trusted network, then Genians designates the Node as a critical one. 
This may go with not only an Agent Control option in Definition configuration settings alone but also a Plugin Agent Action, Control Interface, which broadens Agent's capabilities.
(*Refer to Controlling Endpoints » Controlling Windows » Controlling Network Interface.*)

For running an Agent Action to control an interface, please see :doc:`/endpoints/network-interface` 


Step 1. Configure Settings for Multi-Homed / Ad hoc Network in Anomaly Definition
---------------------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Multi-Homed / Ad hoc Network**
#. Find **Anomaly Event** section to configure more options
#. For **Trusted Network Scope** (*An option may be configurable in Policy > Object > Network.*)
#. For **Sensor Network as Trusted** (*This prevents from not being on the trusted network if a Sensor changes its management scope.*)
#. For **Agent Control** select **Yes** to configure more options and you may specify the followings:

   - **Response:** Disabling Device or Generating Logs
   - **Interface Disabled Notification:** Yes or No
   - **External Device Exceptions:** optional setting to specify the device to be an exception to this Anomaly (*The name must be the exact match, therefore, you had better configure Interface Type Exception instead*)  
   - **Interface Type Exception:** Wired, Wireless or Virtual

#. Click **Update**

Step 2. Create Status Group For Multi-Homed / Ad hoc Network Conected
---------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Multi-Homed / Ad hoc Network Connected
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** Multi-Homed / Ad hoc Network

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect Multi-Homed / Ad hoc Network Through Node Policy
---------------------------------------------------------------

You may assign the Status Group of Spoofed ARP Sent you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **Multi-Homed / Ad hoc Network** pre-configured in Step 1. 
The anomaly, **Multi-Homed / Ad hoc Network**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block Multi-Homed / Ad hoc Network Through Enforcement Policy
---------------------------------------------------------------------

You may assign the Status Group of Multi-Homed / Ad hoc Network Connected you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **Multi-Homed / Ad hoc Network** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.