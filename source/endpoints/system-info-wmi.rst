Collecting Windows System Information using WMI
===============================================

Policy Server communicates with the Agent to use Windows Management Instrumentation (WMI) to obtain Windows system information on end users Windows devices

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect System Information Using WMI** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**
#. For **Namespace**, select appropriate namespace from drop-down or define namespace in **User Defined Namespace**
#. For **WMI Query**, enter in optional queries separated by semicolon
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect System Information Using WMI** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
