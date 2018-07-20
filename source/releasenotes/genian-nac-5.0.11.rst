Genian NAC v5.0.11 Release Notes
================================

**New Feature & Improvement**

- #16828 Added the ability to check the port information used by the product
- #16807 Improve node group matching speed with large number of conditions
- #16564 Added verified node type and platform name functionality
- #17076 The improved to leave the superuser ID and IP as audit records when manually remove the risk
- #16907 Improved validation check order when registering with user’s existing user ID
- #16536 Added Device Lifecycle Management function
- #16575 [Agent] Added ability to monitor system resources (CPU, Memory, Network, Disk) usage

**Bug Fix**

- #17179 Fixed an issue that caused errors in user 2-step authentication in CWP
- #17064 Fixed the problem that automatic reauthentication does not work when authentication is expired while using AD alternate authentication
- #16896 Fixed a problem where the start date end date is initialized when the user input date pattern is not yyyy-MM-dd when searching the audit log
- #16954 Fixed the problem that user list screen of user group is displayed incorrectly
- #16960 Fixed the problem that initial MAC grant does not work when platform is detected when registering new node
- #17033 If node group condition operation is AND, fix problem that satisfies matching condition but does not match actual node
- #17131 [Agent] Fixed the problem that macOS agent plug-in execution is infinitely repeated