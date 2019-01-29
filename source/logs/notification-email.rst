Sending Notification Using Email
================================

Setup Email Account
-------------------

#. Go to **Preferences** in the top panel
#. Go to **General > Miscellaneous** in the left **Preferences** panel

Under **Email**

#. For **Server Address:**, type server address (*e.g. smtp.gmail.com*)
#. For **Server Port:**, type port number (*e.g. SSL=465, TLS/STARTTLS=587*)
#. For **Sender Address:**, type address for sender (*Email Address to be displayed as from*)
#. For **Sender Name:**, type name of sender (*Name to be displayed as from*)
#. For **SSL Connection** (*Turn on if using SSL port*)
#. For **Username**, type username
#. For **Password**, type and re-type password
#. Click **Update**
#. Click **Test** to test configuration settings and send e-mail

You can send notifications to groups when specific logs are generated from specific events.

Send Notifications by Email
---------------------------

.. note:: Administrator email must be configured under **Management** > **User** > **Administrator** > **Notification**.

#. Go to **Log** in the top panel
#. Go to **Log > Log Filter** in the left **Log** panel
#. Select a **Log Filter Name** and click **Edit**
#. Find **Notification** and click **Checkbox** to configure options
#. For **Recipient Administrator**, double-click desired administrator (*Choose Admin Role for a group of Administrators*)
#. For **Recipient Admin Role**, double-click desired role
#. For **Short Message**, type to be added to **Subject** line
#. For **Long Message**, type for contents of message
#. Click **Update**