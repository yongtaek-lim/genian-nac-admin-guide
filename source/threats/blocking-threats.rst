Blocking Threats
================
 
**Network Sensor** listens to network traffic for abnormalities and identifies **Nodes** as having Threats. You can block nodes identified as being a threat in two ways.

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

Step 1. Assign Threat Definitions to Node Policy
------------------------------------------------

By default the Default Policy is collecting information and is not detecting any threats. This will add Threat Definitions to the Default Policy and actively detect threats.

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click on **name of Node Policy** in the main Node Policy window
#. Find **Threat Definition** section. Click **Assign**
#. Select **Threat Definitions** from **Available** column, and move to **Selected** column
#. Click **Add**
#. Click **Update**

Step 2. Create Threat Status Group
----------------------------------

This will group together all devices that will be identified by the default Policy using enabled Threat Definitions

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Unique Name (*e.g. Threat Status Group*)
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Settings** section
#. For each **Threat** you want to add use the following:

   - **Criteria:** Threat
   - **Operator:** Detected is one of
   - **Value:** (*One of the listed threats*)

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Update**

Step 3. Create Enforcement Policy To Block Threats
--------------------------------------------------

This will block all Threats identified within the Default Policy and are listed in the Threat Status Group from Step 2.

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. **Action** tab, click **Next**
#. **General** tab

   - **ID:** Unique Name (*e.g. Threat Policy*)
   - **Description:** Threat Policy to block all devices detected as Threats
   - **Application Mode:** Enabled
   - Click **Next**

#. **Node Group** tab, find and double click **Status Group** (*e.g. Threat Status Group*)
#. **Permission** tab, double click on **PERM-DNS**. Click **Next**
#. **Redirection** tab, click **Next**
#. **Agent Action** tab, click **Finish**   
#. Click **Apply**




