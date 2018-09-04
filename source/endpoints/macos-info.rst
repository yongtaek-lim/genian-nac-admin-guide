Collecting Computer OS Information
==================================

The Network Sensor collects Operating System information from end users macOS devices using the Agent

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect Computer OS Information** in the Agent Action window (*Notice there are two. One for Windows, and another for MacOS*)

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect Computer OS Information** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
