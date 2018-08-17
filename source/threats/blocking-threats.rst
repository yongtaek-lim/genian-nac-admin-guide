Blocking Anomalies
================
 
**Network Sensor** listens to network traffic for abnormalities and identifies **Nodes** as having Anomalies. You can block nodes identified as being a anomaly in two ways.

   - Block Immediately Through IPAM
   - Block Automatically Through Enforcment Policy

Block Nodes Through IPAM
------------------------

#. Go to **Management > Node** in top panel
#. Find **desired Nodes** and click on **Checkboxes**
#. Go to **Tasks > IPAM** and select appropriate action to deny (*Deny IP, Deny MAC, or Deny IP and MAC*)
#. **Node** will now be **highlighted** in pink and have a **strikethrough** the IP, MAC, or both

Unblock Nodes Through IPAM
--------------------------

#. Go to **Management > Node** in top panel
#. Find **desired Nodes** and click on **Checkboxes**
#. Go to **Tasks > IPAM** and select appropriate action to allow (*Allow IP, Allow MAC, or Allow IP and MAC*)
#. **Node** will not be **highlighted** in pink and will not have a **strikethrough** through the IP, MAC, or both

Block Nodes Through Enforcement Policy
--------------------------------------

Step 1. Assign Anomaly Definitions to Node Policy
------------------------------------------------

By default the Default Policy is collecting information and is not detecting any Anomalies. This will add Anomaly Definitions to the Default Policy and actively detect Anomalies.

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click on **name of Node Policy** in the main Node Policy window
#. Find **Anomaly Definition** section. Click **Assign**
#. Select **Anomaly Definitions** from **Available** column, and move to **Selected** column
#. Click **Add**
#. Click **Update**

Step 2. Create Anomaly Status Group
----------------------------------

This will group together all devices that will be identified by the default Policy using enabled Anomaly Definitions

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Unique Name (*e.g. Anomaly Status Group*)
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Settings** section
#. For each **Anomaly** you want to add use the following:

   - **Criteria:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** (*One of the listed Anomalies*)

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Update**

Step 3. Create Enforcement Policy To Block Anomalies
--------------------------------------------------

This will block all Anomalies identified within the Default Policy and are listed in the Anomaly Status Group from Step 2.

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. **Action** tab, click **Next**
#. **General** tab

   - **ID:** Unique Name (*e.g. Anomaly Policy*)
   - **Description:** Anomaly Policy to block all devices detected as Anomalies
   - **Application Mode:** Enabled
   - Click **Next**

#. **Node Group** tab, find and double click **Status Group** (*e.g. Anomaly Status Group*)
#. **Permission** tab, double click on **PERM-DNS**. Click **Next**
#. **Redirection** tab, click **Next**
#. **Agent Action** tab, click **Finish**   
#. Click **Apply**




