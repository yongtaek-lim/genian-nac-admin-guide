Restoring From Existing Backup
==============================

You can restore backups in the event of system failure. To perform this restore process you should have CLI admin access
(*Only available for On-Prem Policy Server but not for the Cloud Version*)

Locate a Backup File and Restore
--------------------------------

#. Click **Preferences** in the top panel
#. Go to **Configuration > Backup** in the left panel
#. Click **Download Backup File** button
#. Copy **Backup** file that you want to restore from the list and then exit out
#. Login to Policy Server through CLI Connecting Command Line Console
#. Type **enable** and **Admin Password** to get into **Global Mode**
#. Enter "do restore <filename> all" to restore backup
