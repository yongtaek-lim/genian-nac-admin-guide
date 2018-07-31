LDAP (Active Directory)
=======================

.. note:: This feature required Enterprise Edition

Creating Synchronization
------------------------

You can synchronize user information with LDAP on a scheduled basis

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Data Synchronization** in the left Preferences panel
#. Click **Tasks > Create**

Under **General**

#. For **ID**, type unique name.
#. For **Update Interval**, select the specified time or periodic interval for this Synchronization.
#. For **Applying Policy**, select **Enabled** for apply change after Synchronization. If there are several synchronization settings, you can set it to Disabled and enable only the last one.

Under **Database**

#. For **Type**, section **LDAP**
#. For **Server Address**, type IP Address or FQDN of Active Directory server
#. For **Server Port**, type AD LDAP service port. by default LDAP port is **389**. if you use LDAPS (LDAP over SSL) default port is **636**.
#. For **SSL Connection**, select **On** if you use LDAPS.
#. For **DB Username**, type Bind DN of Active Directory. normally, you can use email format like administrator@company.com
#. For **DB Password**, type Bind DN user's password

Uder **User Information**

#. For **Table Name**, type distinguished name (DN) of users. normally, CN=Users,DC=company,DC=com
#. For **Where Clause for DB**, type **objectClass=person** for filtering person object.
#. For **Column Name for Username**, type **sAMAccountName**
#. For **Column Name for Full Name**, type **displayName**
#. For any other extra information, you can use LDAP attribute name for each column name.

Testing Synchronization
-----------------------

#. User **Data Synchronization**, click **Tasks > Synchronize Now**

.. attention:: Since the Active directory does not provide the userPassword attribute, the user password can not be synchronized. Therefore, you must set the integration separately. See :doc:`../integrate-external/active-directory` 
