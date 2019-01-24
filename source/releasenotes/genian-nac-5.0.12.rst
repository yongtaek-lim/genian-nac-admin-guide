Genian NAC v5.0.12 Release Notes (February 2018)
================================================

Release Date: 2/8/2018

:download:`Download 5.0.12 <https://www.genians.com/get-files/12761/?version=5.0.12>`

**New Feature & Improvement**

- #17214 Support LSI Logic SAS adapter
- #17156 Improved to send user secondary verification SMS authentication code to 6 digits
- #17095 Support MacOS agent for High Sierra
- #17112 Add account expiration time setting function from user management screen
- #16232 Add ability to gather locally configured IPv6 information with agent installedBug Fix

**Bug Fix**

- #17316 Fixed the problem of not operating the wireless LAN card on Intel NUC NUC6CAY
- #17071 Fixed a problem where the user tries to delete the backup file if free space can not be secured
- #17104 Fixed the problem that mssql.log file is not generated when synchronizing information with MSSQL server
- #17145 Fixed an error that could not be applied to a policy even after entering a value that is out of acceptable range for the node action
- #17128 Fixed a problem where the same device information appears duplicated in USB device information
- #17161 Fixed an issue where agent unassembly nodes were included in the agent information related node group
- #17107 Fixed the problem that the center IP is designated as virtual IP when the virtual IP is automatically set in the center band sensor
- #17128 [Agent]Fixed a problem where tray icon is not displayed when macOS agent is installed
- #17131 [Agent] Fixed an issue where agent authentication window does not exit when Agent Failsafe operation