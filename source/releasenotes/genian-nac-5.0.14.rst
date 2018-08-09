Genian NAC v5.0.14 Release Notes
================================

Release Date: 8/10/2018

For upgrading system software, please see :doc:`/system/system-software` 

**New Feature & Improvement**

- #15257 Improved Captive Web Portal

  - Separate CWP can be applied to each node policy
  - Improved customization
  - Ability to modify CSS and Layout

- #17919 Enabling port mirroring enforcement mode on v5.0
- #16373 Quarantine VLAN ID assignment via RADIUS
- #17599 Export dashboard to PDF format
- #17125 Mobile App for administrator added. Downloadable from "System> Genian Software"
- #17880 Ability to disable IPv6 configuration of network interface Added to agent action
- #17891 Adding a Node Group Condition for the IPv6 Activation Status of an Interface
- #17379 Improved the ability to enable / disable ports on the port scan list screen
- #12581 Improved RADIUS authentication success log to display actual Username instead of anonymous Id
- #17588 Improved agent action execution condition to change according to OS type
- #17635 Added ARP Poisoning Strict Mode option
- #17663 Added function to unlock by authentication code when full screen is locked through agent authentication window action
- #17669 Remove Hyphenation Validation When Entering Cell Phone Numbers
- #17676 Added Bitdefender ANTIVIRUS information collection function to Antivirus information collect action
- #17821 Added ability to gather information about Kaspersky new anti-virus product (Kaspersky Endpoint Security 11 for Windows)
- #17731 RADIUS Configuration Menu Consolidated into the "RADIUS Server" menu
- #17812 Improved to be listed in the selected subnet when returning from node management screen in Matrix view
- #17862 Improved processing performance when deleting multiple sensors
- #17876 Improved problem that difficult to distinguish OS of agent action when node group condition is added
- #17436 macOS agent check condition only Plug-in added.

**Bug Fix**

- #17719 Agent down after trying macOS Agent Update
- #17911 Plug-in does not work if period is specified for periodic execution of agent action
- #18003 api-ms-win-crt-runtime-l1-1-0.dll error when installing agent on a specific PC
- #18153 macOS agent and CWP display authentication status differently
- #17514 Fixed an issue where the alarm on the audit record filter for the new MAC detected does not work
- #17526 Fixed MatrixView tooltips that do not work properly
- #17558 Fixed the problem that the tooltip of macOS agent menu bar icon is broken
- #17640 Some monitor information may only be displayed when using multiple monitors
- #17650 When generate OTP code in QR code in cloud, image break and security key reset button are not visible
- #17696 Fixed problem with 802.1x authentication due to EAP-GTC plugin unregistered on Windows
- #17776 Fixed that SNMP Write community string is always invalid
- #17818 Duplicate contents are sent to the same recipient when sending alarm by audit log filter
- #17868 There is a possibility that both devices can be maintained as Master when the policy server redundancy is configured
- #17926 Corrected time value incorrectly displayed among the collected antivirus information
- #18055 Invalid Agent Action permissions in Basic Edition fixed
- #18117 Fixed a problem where patch download fails if there are multiple interfaces of Policy Server or Distribution Server