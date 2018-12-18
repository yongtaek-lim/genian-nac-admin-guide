Genian NAC v5.0.8 Release Notes (May 2017)
==========================================

Release Date: 5/22/2017

**New Feature & Improvement**

- #15992 – Add user count and link to user group list
- #16015 – Support for MySQL DB connection via SSL when synchronizing user information
- #16134 – Improved to leave audit log when untagged
- #16199 – Improved to separate general and administrative privileges from the CLI
- #16231 – Added “security question” method to lost password recovery method
- #16366 – Added ability to sort node group nodes count
- #16432 – Opensshd Vulnerability Patch (CVE-2016-6210, CVE-2016-6516)
- #16133 – Change the origin of macOS agent from Unknown to identified developer
- #15883 – Notify when the set time zone and browser time zone are different after administrator login
- #15853 – Agent support High DPI on Windows

**Bug Fix**

- #16236 – Layout corruption when modifying dashboard tabs
- #16247 – NTP server settings among DHCP options are sent to DNS entries
- #16280 – Agent custom icons do not work
- #16306 – DB backup file download list incorrectly displays backup file size
- #16310 – Problems that do not show QR code image on OTP authentication screen
- #16335 – Abnormal termination of program when Internet Connection Sharing is controlled by the interface control plug-in
- #16379 – Node Management> Status chart is displayed incorrectly