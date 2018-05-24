Configuring Network Appliance
=============================

You can configure System Appliance Settings for the current installed Policy Server or Default Settings for all new Policy Servers that will be added to the primary Policy Server.

To Configure Appliance Settings
-------------------------------

#. Go to System in top panel
#. Find and click Policy Server IP in the main System window
#. Find and click Appliance tab in the main System window

To Configure Default Appliance Settings
---------------------------------------

(*Settings below are optional and will be default settings for all additional Policy Servers*)

#. Go to System in top panel
#. Go to System Defaults > Network Appliance in the left System Management panel

To Allow Remote Access via SSH
------------------------------

#. Find Security section and enter IP Address(es) for Approved SSH Source IP 1&2 (*e.g. 192.168.1.10, 192.168.1.0/24, 0.0.0.0/0*)
#. Click Update

To Proxy For Windows Updates
----------------------------

#. Find Proxy for Windows Updates section and select On in drop-down
#. Select Network Group for Proxy Service to use
#. Click Update

To Setup SNMP Agent
-------------------

#. Find SNMP Agent section and select On in drop-down
#. Enter the following:
   - Username
   - Authentication Password (*SHA, minimum length – 8 characters*)
   - Privacy Password for data encryption (*AES, minimum length – 8 characters*)
#. Click Update

To Edit Asset Management Thresholds
-----------------------------------

#. Find Asset Management section
#. Enter the following:
   - Data Disk Threshold generates log if Data Disk is over this threshold (*Default is 90*)
   - Memory Threshold generates log if Memory is over this threshold (*Default is 90*)
   - CPU Threshold generates log if CPU is over this threshold (*Default is 95*)
#. Click Update

To Edit System Date And Time
----------------------------

#. Find Date and Time section
#. Select Country and closest City from drop-downs for System Time Zone
#. Click Update

To Change Character Set
-----------------------

#. Find Miscellaneous section
#. Select Character Set from drop-down
#. Click Update
