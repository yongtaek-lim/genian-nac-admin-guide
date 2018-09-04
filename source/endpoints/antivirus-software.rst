Controlling Antivirus Software Settings
=======================================

Policy Server communicates with the Agent to collect information on the Antivirus Software installed on 
end users Windows devices so you can  control scans, and force updates.

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Antivirus Software Settings** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Scheduled Antivirus Software Scan**, adjust frequency to collect information (*Seconds - hours*)
#. For **Real-time Scan Off Events Exceptions**, specify the amount of times for Off Events to not be reported
#. For **Antivirus Software Integration**, turn **On** to integrate with other Anitvirus Software

   - **Generating Mitigation Logs**, select **Generate Logs or Generate Error Logs** to generate mitigation logs
   - **Period for Duplicate Logs Exception**, adjust time to exclude duplicate logs (*Minutes - hours*)
   - **Real-time Scan Enforcement**, select **Off** to disable real-time scanning
   - **Force Scan**, adjust how often to Force Scan (*hours - months. Enter 0 to not enforce*)
   - **Scan Type**, select between **Full or Quick Scan**
   - **Hiding Scanner**, turn **On** to hide the virus scan window from user
   - **Force Update**, adjust how often to Force Update (*hours - months*)
   
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Antivirus Software Settings** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
