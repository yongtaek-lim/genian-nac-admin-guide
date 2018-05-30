Configuring Active Directory
============================

You can configure **Policy Server** to integrate with **Active Directory** for **User Authentication**

To Configure Active Directory Integration
-----------------------------------------

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Authentication Integration** in the left Preferences panel
#. Find **LDAP Authentication Integration** section in the main window
#. Enter the following:

   - **Server Address**:
   - **Server Port**: (*Non-SSL=389, SSL=636*)
   - **Base DN**: (*e.g. CN=Users,DC=genians,DC=com*)
   - **Bind DN**: (*Should be FQDN: e.g. Administrator@.com*) (*Bind Account should have Administrator Privileges*)
   - **Bind Password**:
   - **User Naming Attribute**: (*e.g. sAMAccountName*)
   - **SSL Connection**: (*Turn on if using SSL port 636*)

#. Click **Update**
#. Click **Test** to test configuration settings (*Test account can be any User Account found within the Base DN*)

To Synchronize Data With Active Directory
-----------------------------------------

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Data Synchronization** in the left Preferences panel
#. Go to **Tasks > Create**
#. Enter the following:

   - **ID**:
   - **Description**:
   - **Frequency**: (*How often do you want to schedule this to run*)
   - **Action**: (*Should be Enabled by default*)
   - **Type**:
   - **Server Address**:
   - **Server Port**: (*Non-SSL=389, SSL=636*)
   - **SSL Connection**: (*Turn on if using SSL port 636*)
   - **DB Username**: (*Should be FQDN: e.g. Administrator@.com*) (*Bind Account should have Administrator Privileges*)
   - **DB Password**:

#. Click **Save**
#. Click **Checkbox > Tasks > Synchronize Now** to synchronize Data now
