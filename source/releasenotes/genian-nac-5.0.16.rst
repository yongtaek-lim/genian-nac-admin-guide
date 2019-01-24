Genian NAC v5.0.16 Release Notes (January 2019)
===============================================

Release Date: 1/7/2019

:download:`Download 5.0.16 <https://www.genians.com/get-files/12761/?version=5.0.16>` 

For instructions on installing and updating Genian NAC, please see :doc:`/system/system-software`  

New Features and Improvements
-----------------------------

- #12840 Added Sensor-based IPv6 support 
  You may now find IPv6 enabled Nodes detected via Network Sensor and configure Node Group Condition settings accordingly to block IPv6 Nodes as needed.

 .. image:: /images/ipv6_popup.png
    :width: 600px

- #18273 Scheduled export of Dashboard Report to PDF and email delivery 
  You may now export a Dashboard using PDF format and configure the Dashboard Report settings to be scheduled and emailed.

 .. image:: /images/dashboard_report.png
    :width: 500px
    
- #18234 User authentication execution time monitoring and processing delay warning function added
- #18182 Display SSID information of Node when RADIUS Accounting SSO is enabled
- #12441 Improved problem that does not display version information by Agent platform in Widgets and Status
- #17638 Added Google mail server (Google OAuth2 authentication) when setting outgoing mail server for mail notifications
- #17855 Improved to select Antivirus name when creating Node Group conditions for Antivirus information
- #18034 Term changed, Threat -> Anomaly
- #18201 Added Authorization header Settings to Log Filter Webhook settings

Issues Fixed in 5.0.16
----------------------

- #18418 OS update via NAC Proxy does not work on Windows 10
- #18164 CLI vlan setting does not work if input is long
- #18260 Some programs are not removed by the Uninstall Program
- #18312 Wireless Connection Manager can not connect to 802.1x (GTC) when deleting GnEapGTC.dll from system folder
- #18334 Fixed an issue where Node information would not remain in the Log when the tag was automatically removed due to expiration
- #18368 Fixed an error of duplicate click events for Submit button when submitting for IP Request
- #18370 Agent did not work properly after installing IPv6 feature in Windows XP Fixed
- #18411 Device Name / Device Description of Node Group Condition settings do not work properly and the duplicate Condition Criteria have been fixed
- #18597 Critical interface blocking for virtual interfaces not working
- #18473 Improved to remove if the Node information detected by the network scan is no longer valid