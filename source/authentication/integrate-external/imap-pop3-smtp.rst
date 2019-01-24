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

Troubleshooting
---------------

.. error:: **Gmail SMTP Integration known issue:** 

                * Authentiction Test: Authentication failed.Authentication failed.SMTP(535-5.7.8:Username and Password not accepted. Learn more at 535 5.7.8 https://support.google.com/mail/?p=BadCredentialsy32sm41405227qt)
                * Genian NAC log : 	Login failed. ERRMSG='Authorize(Account disabled)'
                * **Fix:** Turn on Less secure app access in Google account settings / security
 
