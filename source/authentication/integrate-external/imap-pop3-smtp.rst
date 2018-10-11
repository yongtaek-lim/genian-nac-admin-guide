Mail Server
============

EMAIL is the service provided by most organizations, making it the easiest to provide the user directory.
You can check the user's username and password using **SMTP**, **POP3**, and **IMAP**, which are used in EMAIL.

IMAP
----

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Authentication Integration** in the left Preferences panel
#. Find **IMAP Authentication Integration** section in main window
#. Enter in **Server Address**, **Server Port**, and **Domain Name**
#. Click **Update**
#. Click **Test** to test configuration settings

**Examples**

============================ ===================== ======== ==============
Service Name                 Server Name           Port     Domain
============================ ===================== ======== ==============
Google G Suites              imap.gmail.com        993      Your Domain
Exchange Online (Office 365) outlook.office365.com 993      Your Domain
============================ ===================== ======== ==============

POP3
----

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Authentication Integration** in the left Preferences panel
#. Find **POP3 Authentication Integration** section in main window
#. Enter in **Server Address**, **Server Port**, and **Domain Name**
#. Click **Update**
#. Click **Test** to test configuration settings

**Examples**

============================ ===================== ======== ==============
Service Name                 Server Name           Port     Domain
============================ ===================== ======== ==============
Google G Suites              pop.gmail.com         995      Your Domain
Exchange Online (Office 365) outlook.office365.com 995      Your Domain
============================ ===================== ======== ==============

SMTP
----

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Authentication Integration** in the left Preferences panel
#. Find **SMTP Authentication Integration** section in main window
#. Enter in **Server Address**, **Server Port**, and **Domain Name**
#. Click **Update**
#. Click **Test** to test configuration settings

.. note:: Genian NAC currently support only smtps (SMTP over SSL)

**Examples**

============================ ===================== ======== ==============
Service Name                 Server Name           Port     Domain
============================ ===================== ======== ==============
Google G Suites              smtp.gmail.com        465      Your Domain
============================ ===================== ======== ==============