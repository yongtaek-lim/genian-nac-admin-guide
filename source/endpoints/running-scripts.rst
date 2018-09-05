Run Script
==========

You can setup Batch or VB scripts to run on the end users Windows devices

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Run Script** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value** 

Under **Plugin Settings** section

#. For **Script Format**, specify a script format to run (*VB Script, Batch Script*)
#. For **Script**, type and enter script to be run
#. For **Account Options**, specify an account to run a script from drop-down
#. For **Restart Options**, specify whether to Prompt or Restart
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Run Script** in the **Available** section. Select and drag it into the *Selected* section
#. Click **Add**
#. Click **Update**
