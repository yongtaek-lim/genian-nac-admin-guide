Configuring User Authentication by Agent
========================================

**Agent** not only assists in determining the posture of the endpoint device, but can also collect system information, access control, and authenticate users. You can configure the **Policy Server** to force users to authenticate using the **Agent** with the **Authenticate User Using Genian Agent** plugin. Once Users credentials have been Authenticated the **Agent** then communicates with the Policy Server every 2 minutes continually validating the User behind the endpoint device.

Step 1. Create Node Group for Authentication by Agent
-----------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Group > Node** in the left Policy panel
#. Click **Tasks > Create New Policy Group**
#. Enter **ID** as **Agent Authentication**
#. Find **Condition** section in the Node Group window. Click **Add**
#. Enter the Following:

   - Criteria: **Agent**
   - Operator: **is**
   - Value: **Installed**

#. Click **Save**
#. Click **Apply** in the top right. Click Close

Step 2. Create Node Policy for Agent Authentication
---------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Tasks > Create**. Complete steps in **Node Policy Wizard**
#. On **General** tab. Enter **ID** as **Agent Authentication**
#. On **Node Group** tab. Select **Agent Authentication** Node Group and move it to **Selected** column
#. On **Preferences** tab. Enter in **desired Options**
#. On **Agent Action** tab. Select **Authenticate User Using Genian Agent** and move to **Selected** column
#. On **Threat Definition** tab. (*Nothing required on this tab*)
#. Click **Finish**
#. Click **Apply** in the top right. Click Close

Step 3. Configure User Authentication by Agent Plugin
-----------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Authenticate User Using Genian Agent**
#. Add **desired Conditions** and **Agent Actions**
#. Click **Update**
#. Click **Apply** in the top right. Click **Close**

(*Steps below are optional to use an existing Node Policy if you prefer not to create a new one*)

Step 4. Assign Agent Action to Node Policy
------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click **Node Policy** name
#. Find **Agent Action** section. Click **Assign**
#. Locate **Authenticate User Using Genian Agent** and move to **Selected** column
#. Click **Add**
#. Click **Apply** in the top right. Click Close

Remove Agent Action from Node Policy
------------------------------------

#. Go to **Policy** in top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click **Node Policy name**
#. Find **Agent Action** section. Locate **desired Agent Action** to remove and click **Delete** far right
#. Click **Apply** in the top right. Click Close
