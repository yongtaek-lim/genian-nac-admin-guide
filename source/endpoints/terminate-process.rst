Terminate Process
=================

You can kill specific processes that are running on the end users Windows devices and schedule 
the frequency to verify that they continue to not run

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Terminate Process** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Process Terminated Event Notification**, turn **On** to notify a user when a process is terminated

   - **Contents**, type to enter contents to terminate a specific process

#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*) 
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Terminate Process** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
