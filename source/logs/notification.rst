Sending Notifications
=====================

Policy Server can send Notifications to administrators, end users, networking devices, 
and third-party security products using various protocols. (*To do this an Email Account needs to be configured on the Policy Server*)

To Setup Email Account
----------------------

#. Go to **Preferences** in the top panel
#. Go to **General > Miscellaneous** in the left **Preferences** panel
#. Find **Email** section in the main window
#. Enter the following:
   - **Server Address:** (*e.g. smtp.gmail.com*)
   - **Server Port:** (*e.g. SSL=465, TLS/STARTTLS=587*)
   - **Sender Address:** (*Email Address to be displayed as from*)
   - **Sender Name:** (*Name to be displayed as from*)
   - **SSL Connection** (*Turn on if using SSL port*)
   - **Username**
   - **Password**
#. Click **Update**
#. Click **Test** to test configuration settings and send e-mail

.. toctree::
   :maxdepth: 2

   notification-event
   notification-snmp
   notification-syslog
   notification-webhook