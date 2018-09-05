Controlling WLAN
================

Policy Server communicates with the Agent to collect SSID information. You can control the WLAN 
by blocking unauthorized SSIDs, and message users with pop-up notifications

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control WLAN** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value** 

Under **Plugin Settings** section

#. For **SSID Information Scope**, collects information about Detected SSIDs from a WLAN Interface and Connected SSIDs to a WLAN Interface
#. For **Collecting Connections History**, turn **On** to collect information about the wireless connection history

   - **Time Range for Daily Update**, specify the time range to update the wireless connection history (*e.g. 0:00-23:59*)
   - **Attempts**, specify number of days to ry and collect connections history (*If the info cannot be sent, it will update on startup*)
   - **Duration**, specify the time duration in hours for the collected connections history

#. For **Disabling Wireless Connection**, specify whether to disable the wireless connection not allowed

   - **How to Define Allowed SSIDs**, select how to define SSIDs to be allowed (*Selecting WLAN Group, Entering SSIDs, Using Regular Expression*)
   - **Allowed WLAN Group**, select a WLAN Group to be allowed from drop-down
   - **Delay**, specify the time of how long disabling connection not allowed is delayed (*seconds - minutes*)
   - **Disabled Connection Notification and Resolution**, specify whether to notify a user and how to resolve the connection disabled from drop-down
   - **Auto-Connect to Allowed SSIDs**, specify whether to automatically connect to SSIDs allowed (*Windows Vista or above required*)

#. For **Disabling AP Mode**, specify whether to disable AP mode such as SoftAP or Ad-hoc for wireless network interface

   - **Interface Disabled Event Notification**, turn **On** to notify a user for the wireless AP mode disabled

#. Enter in **CWP message**, **Conditions**, and adjust **Agent Actions** based off of your network requirements
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control WLAN** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
