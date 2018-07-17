Enabling RADIUS Authentication
==============================
 
You can configure the Genian NAC Policy Server to use it’s built-in RADIUS Server to act the same as integrating with an external RADIUS Server.

To Enable Built-In RADIUS Authentication
----------------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. Find **RADIUS Server** section in the main window
#. Enter the following:

   - **Shared Secret Key** and retype
   - **RADIUS Client IP** (*IP address or addresses to be allowed as Clients*)
   - **Server Port** (*e.g. 1812*)
   - **EAP Authentication** (*Default is on. Select EAP type in drop-down*)
   - **MAC Authentication**
   - **Accounting** (*RADIUS Accounting for NAS*)

#. Click **Update**

To Enable AD Account for RADIUS
-------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. Find **RADIUS Server: AD Account** section and select **On** in drop-down
#. Enter the following:

   - **Domain Name** (*e.g. genians.com*)
   - **Username** (*Default is Administrator. Account needs to have Admin Privileges*)
   - **Password** and retype

#. Click **Update**

To Enable URL Account for RADIUS
--------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. Find **RADIUS Server: URL Account** section and select **On** in drop-down
#. Enter the following:

   - **URL** (*e.g. http://.com*)
   - **Methods** (*GET, POST*)
   - **Regex for Authentication** (*This regular expression will check for successful login*)

#. Click **Update**

To Enable Email Authentication for RADIUS
-----------------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. Find **RADIUS Server: Email Authentication** section and select **On** in drop-down
#. Need IMAP/POP3/SMTP configured, :doc:`imap-pop3-smtp`
#. Click **Update**

.. toctree::
   :maxdepth: 1

   mac-authentication
