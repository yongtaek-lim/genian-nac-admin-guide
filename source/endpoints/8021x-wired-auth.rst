Configuring 802.1x Wired Authentication
=======================================

802.1x is an IEEE Standard Switch-Port Authentication which provides assurance that a person claims to be behind an Endpoint Device. In the wired environment, this is a physical port on a switch. In a wireless environment, it is an association with an Access Point(AP). Port-Based Authentication is that an Endpoint Device attempting to connect to a network will use an 802.1x supplicant and be challenged at the point of connection using EAP messages before communication with any other internal network devices can start.
You can configure the Policy Server to authenticate users access through 802.1x.

Step 1. Create Node Group for Authentication by 802.1x
------------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Group > Node** in the left Policy panel
#. Click **Tasks > Create New Policy Group**
#. Enter **ID** as **802.1x Authentication**
#. Find **Condition** section in the Node Group window. Click **Add**
#. Enter in the Following:

   - Criteria: **IP**
   - Operator: **is one of subnet**
   - Value: **(Network Subnet)**

#. Click **Save**
#. Click **Apply** in the top right. Click Close

Step 2. Create Node Policy for 802.1x Authentication
----------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Tasks > Create**. Complete steps in **Node Policy Wizard**
#. On **General** tab. Enter **ID** as **802.1x Authentication**
#. On **Node Group** tab. Select **802.1x Authentication** Node Group and move it to **Selected** column
#. On **Policy Preferences** tab. Enter in **desired Options**
#. On **Agent Action** tab. Select **Configuring 802.1X Wired Authentication** and move to **Selected** column
#. On **Threat Definition** tab. (*Nothing required on this tab*)
#. Click **Finish**
#. Click **Apply** in the top right. Click Close

Step 3. Configure 802.1X Wired Authentication Plugin
----------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Configuring 802.1X Wired Authentication**
#. Add **desired Conditions** and **Agent Actions**
#. Click **Update**
#. Click **Apply** in the top right. Click Close

(*Steps below are optional to use an existing Node Policy if you prefer not to create a new one*)

Step 4. Assign Agent Action to Node Policy
------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click **Node Policy name**
#. Find **Agent Action** section. Click **Assign**
#. Locate **Configuring 802.1X Wired Authentication** and move to **Selected** column
#. Click **Add**
#. Click **Apply** in the top right. Click Close

Remove Agent Action from Node Policy
------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click **Node Policy name**
#. Find **Agent Action** section. Locate **Configuring 802.1X Wired Authentication** and click **Delete** far right
#. Click **Apply** in the top right. Click Close
