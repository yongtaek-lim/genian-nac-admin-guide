MAC+IP Clones
=============

Genian NAC can detect MAC / IP theft in a variety of ways. The Network Sensor periodically sends an ARP request to check the operation status of Nodes. 
If two replies are received at the same time, Genians suspects the MAC / IP clones and designates the Node as a critical Node. 
In addition, if the user changes the MAC on the endpoint where the Agent is installed and the MAC is already being used by another device, that device is then designated as a critical Node.
Genian NAC provides industry-leading platform detection to detect when a Node is changing to another platform, allowing administrators to see when changes are made, and to block devices when unauthorized platform changes are detected.


Step 1. Configure Settings for MAC+IP Clones in Anomaly Definition
------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **MAC+IP Clones**
#. Find **Anomaly Event** section to configure more options

   - For **MAC Spoofing Detection**, optional setting to specify whether an interface's MAC address is manually changed is also detected

#. Click **Update**

Step 2. Create Status Group For MAC+IP Cloned
---------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** MAC+IP Cloned
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** MAC+IP Clones

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect MAC+IP Clones Through Node Policy
------------------------------------------------

You may assign the Status Group of Spoofed ARP Sent you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **MAC+IP Clones** pre-configured in Step 1. 
The anomaly, **MAC+IP Clones**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block MAC+IP Clones Through Enforcement Policy
------------------------------------------------------

You may assign the Status Group of MAC+IP Cloned you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **MAC+IP Clones** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.