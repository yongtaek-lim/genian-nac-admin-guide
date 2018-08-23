Sending Notification Using Event
================================

You can send notifications to groups when specific logs are generated from specific events.

Send Notifications
------------------

#. Go to **Log** in the top panel
#. Go to **Log > Log Filter** in the left **Log** panel
#. Select a **Log Filter Name** and click **Edit**
#. Find **Notification** and click **Checkbox** to configure options
#. For **Recipient Administrator**, double-click desired administrator (*Choose Admin Role for a group of Administrators*)
#. For **Recipient Admin Role**, double-click desired role
#. For **Short Message**, type to be added to **Subject** line
#. For **Long Message**, type for contents of message
#. Click **Update**

Create a Network Sensor Disconnected Log Filter and Notification
----------------------------------------------------------------

#. Go to **Log** in the top panel
#. Go to **Logs** in the left **Log** panel

Under **Search**

#. For **Type:** (*Leave Logs checked*)
#. For **Period:** (*Leave default*)
#. For **Description:** type "Sensor Status changed to down"
#. Click **Search** (*Nothing may appear as the Sensor or Sensors may have never been detected as down*)
#. Click **Save As** (*New Window will appear and enter the following:*)

Under **Log Filter: Create**

#. For **Name:** (*e.g. Network Sensor Disconnected*)
#. For **Description:**, type what this filter will do
#. For **Tree & Log Monitor** (*Leave checked to display Time, Type, Log ID, Detected by, IP*)
#. For **Notification**, click **Checkbox**
#. For **Recipient**, select Administroator or Role
#. For **Short Message:** (*e.g. Network Sensor reported as being disconnected*)
#. For **Long Message:** (*e.g. Network Sensor reported as being disconnected. Network Engineer needs to investigate this issue.*)
#. Click **Save**

Add Macros To Log Notifications Message Box
-------------------------------------------

Genian NAC uses Macros as a placeholder text that gets replaced with specific data when inserted into the 
Log Notifications message box. You can add and customize these Macros to present the data however you like. 
If the Log Notifications message block is left empty then a default set of Macros will be used.

#. Go to **Preferences** in the top panel
#. Go to **General > Log** in the left **Preferences** panel
#. Find **Log Options: Remarks column Elements** section in main **Log** panel
#. Select options to **Enable** this data to be added to **Logs** (*Node Status Logs and Agent Status Logs are optional*)
#. Go to **Log** in the top panel
#. Go to **Log Filter** in the left **Log** panel
#. Find and click **Log Filter Name**
#. Click Edit at the bottom of **Status & Filters** section
#. Find **Notification: Long Message** section
#. Add additional **MACROs** in the **Long Message** block
#. Find and click **Help for Macro** button just above **Notification** section title
#. Choose the desired **MACRO** to add to the message body of the notification (*Some Message{_SWNAME}{SWPORT}*)
#. Click **Update**

(*If Message box is blank then a default of {_DATETIME}{_LOGTYPE}{_LOGID}{_SENSORNAME}{_IP}{_MAC}{_FULLMSG}{_DETAILMSG} 
will be displayed and you can add in additional Macros and customize as desired*)
