Ad Hoc Network Connected
========================

A Genian Agent can immediately detect a multi-homed configuration and Ad hoc network connection in a variety of ways.
If a computer having more than one IP address configured connects to more than one network and one of them is not on the trusted network, then Genians designates the Node as a critical one. 
This may go with not only an Agent Control option in Definition configuration settings alone but also a Plugin Agent Action, Control Interface, which broadens Agent's capabilities.
(*Refer to Controlling Endpoints » Controlling Windows » Controlling Network Interface.*)

For running an Agent Action to control an interface, please see :doc:`/endpoints/network-interface` 

Step 1. Configure Threat Definition Settings for Ad Hoc Network in Threat Definition
------------------------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Threat Definition** in the left Policy panel
#. Click **Ad Hoc Network Connected**
#. Find **Threat Definition Settings** section
#. Specify **Trusted Network Scope** (*An option may be configurable in Policy > Object > Network.*)
#. Specify **Sensor Network as Trusted** (*This prevents from not being on the trusted network if a Sensor changes.*)
#. Select **Yes** to configure more options for Agent Control
#. For **Agent Control** you may specify the followings:

   - Response, you can choose either "Disabling Device" or "Generating Logs"
   - Interface Disabled Notification
   - External Device Exceptions, you can enter a device name (*The name must be the exact match, therefore, you may also configure Network Exceptions by specifying the network type, wired or wireless, instead*)
   - Network Exceptions, you can choose one of No Exceptions, Wired or Wireless

#. Click **Update**

Step 2. Create Status Group For Ad Hoc Network Connected
--------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "Ad Hoc Network Connected", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **Ad Hoc Network**

#. Click **Update**
   
Step 3. Create Node Policy For Ad Hoc Network
---------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "Ad Hoc Network Connected", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **Ad Hoc Network Connected Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** (*Or you may select configured Agent Action* **Control Network Interface**)
#. On **Threat** tab, select **Ad Hoc Network**
#. Click **Finish**

