Collecting Network Information
==============================

Policy Server communicates with the Agent to collect network information on the end users Windows devices

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect Network Information** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings**

#. For **Traffic Utilization Change Threshold**, change the percentage for bandwidth to trigger network traffic utilization
#. For **Update Interval**, adjust Periodic Interval (*Seconds - hours*)
#. For **Moving Average**, adjust the moving time to be greater then the Update Interval
#. For **Collecting Open Port Information**, turn **On** to collect open port information
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect Network Information** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
