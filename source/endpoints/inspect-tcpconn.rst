Inspecting TCP Connections
==========================

Policy Server communicates with the Agent to collect TCP Connection Information periodically and disables a network interface that exceeds the configured connection limits.

Add the Agent Action to a Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Inspect TCP Connections** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Inspect TCP Connections
-----------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Inspect TCP Connections** in the Agent Action window
#. Enter in **Conditions**, optional settings

Under **Update Interval**

#. For **Update Interval**, Specify the time interval to update the TCP connection information (0: No Update)
#. For **Connections Change Threshold**, Specify the percentage change in bandwidth to trigger TCP connection information update (excluding LISTENNING)
#. For **Connections Threshold**, Specify the number of connections to be considered as TCP connection information

Under **Interface Control**

#. For **Interface Control**, Specify whether to disable an interface if the connections exceed the specified limit

Under **Interface Disabled Event Notification**

#. For **Interface Disabled Event Notification**, Specify how to notify a user for the event of disabling an interface if the connections exceed the specified limit
#. Click **Update**
