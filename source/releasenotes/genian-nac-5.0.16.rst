Genian NAC v5.0.16 Release Notes (Coming Soon)
==============================================

Release Date: 12/21/2018

For upgrading system software, please see :doc:`/system/system-software` 

New & Enhanced Features
-----------------------

- #12840 IPv6 node detection via network sensor and related node group condition added. Now you can find and block IPv6 enabled nodes

 .. image:: /images/ipv6_popup.png
    :width: 600px

- #18273 Added dashboard periodic PDF export and email delivery
- #18234 User authentication execution time monitoring and processing delay warning function added. Monitor processing delay when setting up external authentication integration
- #18182 Display SSID information of node when RADIUS Accounting SSO is enabled
- #12441 Improved problem that does not display version information by agent platform in widgets and status
- #17638 Add support OAuth2 mail server (like Google) when setting outgoing mail server
- #17855 Improved to select Anti-virus name when creating node group condition for Anti-virus information
- #18034 Terminology change. Threat -> Anomaly
- #18201 Add Authorization header Settings to Log Filter Webhook Settings

Bug Fixes
---------

- #18418 Fixed an issue where OS update via NAC Proxy could not work on Windows 10
- #18164 CLI vlan setting does not work if input is long
- #18260 Some programs are not removed by the uninstall program agent action
- #18312 Wireless Connection Manager can not connect to 802.1x (GTC) when deleting GnEapGTC.dll from system folder
- #18334 Fixed an issue where node information would not remain in the audit trail when the tag was automatically released due to expiration
- #18368 Fixed an error that repeatedly selected application button when applying for IP request application
- #18370 Agent did not work properly after installing IPv6 feature in Windows XP Fixed
- #18411 Node Group Condition Equipment Name / Equipment Description Problems with duplicate problems and conditions that are not working have been fixed
- #18597 Fixed an issue where interface blocking for virtual interfaces did not work
- #18473 Fixed an issue where some network scans did not remove detected node information if it was no longer valid