Blocking Anomalies
==================
 
**Network Sensor** listens to network traffic for abnormalities and identifies **Nodes** as having anomalies. 
You can automatically block Nodes identified as being an anomaly in two ways.

   - Identify Nodes through IPAM and Block them through Denied by IPAM of Enforcement Policy
   - Identify Nodes through Node Group and Block them through New Enforcment Policy
   

Identify Nodes through IPAM and Block them through Denied by IPAM of Enforcement Policy
---------------------------------------------------------------------------------------

You may use IPAM actions and an existing Enforcement Policy, Denied by IPAM accordingly.

Step 1. See Anomalies Detected and Configure IPAM Settings
----------------------------------------------------------

You may be able to see the anomalies detected in a variety of ways. Please see :doc:`/threats/detecting-threats`

#. Go to **Management > Node** in top panel
#. Find **desired Nodes** (or **Anomalies**) and click on **Checkboxes**
#. Go to **Tasks > IPAM** and select appropriate action to deny (*Deny IP, Deny MAC, or Deny IP and MAC*)
#. **Node** will now be **highlighted** in pink and have a **strikethrough** the IP, MAC, or both

Step 2. Assign Denied by IPAM of Enforcement Policy To Block Anomalies
----------------------------------------------------------------------

This will block all Anomalies identified within the IPAM settings configured from Step 2.

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Find **Denied by IPAM**
#. Click **Denied by IPAM** to change its configuration settings as needed 
   (*This Enforcement Policy is not dedicated to block anomalies. Please see :doc:`/ipmac-control`*)

Unblock Nodes through IPAM
--------------------------

#. Go to **Management > Node** in top panel
#. Find **desired Nodes** and click on **Checkboxes**
#. Go to **Tasks > IPAM** and select appropriate action to allow (*Allow IP, Allow MAC, or Allow IP and MAC*)
#. **Node** will not be **highlighted** in pink and will not have a **strikethrough** through the IP, MAC, or both


Identify Nodes through Node Group and Block them through New Enforcment Policy
------------------------------------------------------------------------------

You may create a dedicated Node Group and an Enforcement Policy accordingly.

Step 1. Create Anomaly Status Group
-----------------------------------

This will group together all Nodes that will be identified by the default Policy using enabled Anomaly Definitions

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Unique Name (*e.g. Anomaly Status Group*)
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add, use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** (*One of the listed Anomalies*)

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**

Step 2. Create Enforcement Policy To Block Anomalies
----------------------------------------------------

This will block all Anomalies identified within the Node Policy and are listed in the Anomaly Status Group from Step 1.

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. **Action** tab, click **Next**
#. **General** tab

   - **ID:** Unique Name (*e.g. Anomaly Enforcement Policy*)
   - **Description:** Anomaly Policy to block all Nodes detected as Anomalies
   - **Status:** Enabled
   - Click **Next**

#. **Node Group** tab, find and double click **Status Group** (*e.g. Anomaly Status Group*)
#. **Permission** tab, double click on **PERM-DNS**. Click **Next**
#. **Redirection** tab, click **Next**
#. **Agent Action** tab, click **Finish**   
#. Click **Apply**