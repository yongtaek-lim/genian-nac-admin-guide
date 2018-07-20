Genian NAC v5.0.13 Release Notes
================================

Release Date: 4/18/2018

**New Feature & Improvement**

- #17206 Improved policy server to enable external connections through Proxy server setting.
- #17088 Improved to leave audit records before certificate expiration.
- #17127 Add CUBRUD DB to DB list that can synchronize information.
- #17253 Add the ability to check the allowed IP when the administrator logs in for the first time.

**Bug Fix**

- #17394 Fixed a problem where html tag is output when password input error of computer name change (agent action).
- #17425 Fixed a problem where the CWP URL could not be set if the CWP domain configuration contained a detailed address after ‘/’.
- #17393 Fixed problem where search condition is initialized when audit log filter is modified.
- #17407  Fixed a problem that the host name of the node is continuously changed by the MDNS packet.
- #17230  Fixed a problem where the platform information of the node where the agent is installed is displayed as “Unknown” on the terminal with the latest operating system installed.
- #17424 Fixed a problem that when the version information is compared with the execution condition of the action, the version does not work if the version is only a number without the delimiter.
- #17452[Agent]Corrected the display error status of IPv4 and IPv6 in Windows node interface information.
- #17362Agent] Fixed a problem where macOS agent remote agent deletion hidden function does not work.
- #17378 [Agent] Fixed a problem where NAT was detected when changing the IP of a PC with macOS agent installed.
