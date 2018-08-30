Manage Files
============

You can manage files on the Windows devices by copying, deleting, moving, and renaming files. You can also run specific files

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Manage Files** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Source Path**, specify a source file to be managed
#. For **Management Action**, specify action to take on source file (*Run, Delete, Copy, Move, Rename*)

   - **CLI Parameter**, specify a command line parameter

#. For **Account Options**, specify a account to manage file from drop-down
#. For **Restart Options**, specify whether to Prompt or Restart
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*) 
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Manage Files** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
