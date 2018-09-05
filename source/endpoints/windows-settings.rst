Configuring Windows Security Settings
=====================================

Policy Server communicates with the Agent to configure the Windows Security Settings on end users Windows devices. 
You can disable Guest Accounts, turn on Windows Firewall, block specific inbound ports (e.g. UDP/5355), turn off 
Remote Desktop, control Autorun settings, and setup sync with NTP

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Configure Windows Security Settings** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Disabling Guest Account**, turn **On** to disable the use of Guest Accounts
#. For **Firewall Control**, select **Turn On** to enable Windows Firewall
#. For **Remote Desktop**, select **Disable** to disable to use of Remote Desktop
#. For **Autorun**, select **Disable** to disable autorun on external devices (*Media, External Device, Others*)
#. For **Internet Time Synchronization**, select **Turn On** to synchronize with NTP server. Enter **IP Address** and specify **Synch Interval**
#. For **Require a password on wakeup**, select **Turn On** to enable a password to be required upon wakeup
#. For **Scheduled Task for Windows XP**, select **Disable** to control scheduled tasks for Windows XP only
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Configure Windows Settings** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
