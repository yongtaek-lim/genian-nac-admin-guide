Changing Computer Name
======================

You can control the name of the Windows device

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Change Computer Name** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Computer Name**, specify a computer name to change (*Characters cannot exceed 15 and cannot contain spaces or minus sign(-)*)
#. For **Restart Options**, specify whether to Prompt or Restart

   - **Delaying Computer Restart**, specify time to postpone a restart (*seconds - hours*)

#. For **Agent Execution Account**, specify an account that can change a computer name from drop-down

#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*) 
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Change Computer Name** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
