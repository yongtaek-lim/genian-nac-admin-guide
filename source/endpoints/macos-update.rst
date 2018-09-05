Update macOS
============

You can control whether the macOS device is getting updates and how often. You can also determine 
the action of whether to install updates automatically, or just download updates to allow the user 
to install on their own

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Update macOS** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Execution Interval**, specify the time interval to execute an action on a scheduled basis (*hours - months*)
#. For **Scheduled Check**, turn **On** to check for updates on a scheduled basis
#. For **Operation Mode**, specify whether to check for updates or to install the updates

   - **Scheduled Installation**, specify whether to install the updates on a scheduled basis

#. For **Restart Options**, specify whether to Prompt or Restart
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find Update macOS in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
