Remove Programs
===============

You can control software on your Windows devices by removing programs that you do not allow

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Remove Programs** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value** 

Under **Plugin Settings** section

#. For **Program**, specify a program to be installed on the endpoints and list in Control Panel to be uninstalled
#. For **Notification Before Uninstalling**, specify whether to notify a user before uninstalling a program

   - **Contents**, add contents to notify user
   
#. For **Account Options**, specify a account to remove a program from drop-down
#. For **Restart Options**, specify whether to Notify User or Auto-Restart

#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Remove Programs** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
