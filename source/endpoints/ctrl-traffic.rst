Controlling Network Traffic
===========================

Policy Server communicates with the Agent to collect TCP Connection Information periodically and disables a network interface that exceeds the configured connection limits.

Add the Agent Action to a Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Controlling Network Traffic** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Controlling Network Traffic
---------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Controlling Network Traffic** in the Agent Action window
#. Enter in **Conditions**, optional settings

Under **Network Traffic Control**

#. For **Update Interval**, Specify the time interval to update the network traffic information
#. For **Total Threshold**, Specify the total traffic for its limit
#. For **Incoming Threshold**, Specify the Incoming traffic for its limit
#. For **Outgoing Threshold**, Specify the Outgoing traffic for its limit

Under **Notification**

#. For **Interface Disabled Event Notification**, Specify how to notify a user for the event of disabling an interface if the connections exceed the specified limit
#. Click **Update**
