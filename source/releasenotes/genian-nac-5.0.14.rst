Genian NAC v5.0.14 Release Notes
================================

Release Date: 8/13/2018

For upgrading system software, please see :doc:`/system/system-software` 

New Features
------------

- `#17919`_ Enabled Port Mirroring enforcement mode
- `#16373`_ Quarantine VLAN ID assignment via RADIUS
- `#17599`_ Export Dashboard to PDF format
- #17125 Mobile App. for Administrator
- `#17880`_ Ability to disable IPv6 configuration of Network Interface added to Agent Action
- #17891 Added a Node Group Condition for the IPv6 Activation Status of an Interface
- #17635 Added ARP Poisoning Strict Mode option
- `#17663`_ Added function to unlock by Authentication Code when Screen Lock is applied through agent authentication window action
- #17436 macOS agent Scan Condition Settings added

Enhancements
------------

- #15257 Improved Captive Web Portal. (Separate CWP can be applied to each node policy, Improved customization, Ability to modify CSS and Layout)
- #17379 Improved the ability to Enable/Disable ports in the Port Scan list
- #12581 Improved RADIUS Authentication success log to display actual Username instead of anonymous ID
- #17588 Improved Agent Action Execution Condition to change according to OS Type
- #17669 Removed Hyphenation Validation when entering Cell Phone Numbers
- #17676 Added Bitdefender Anitvirus information collection function to Collect Antivirus Information action
- #17821 Added Kaspersky Antivirus information collection function to Collect Antivirus Information action (Kaspersky Endpoint Security 11 for Windows)
- #17731 RADIUS Configuration options consolidated into the "RADIUS Server" menu
- #17812 Improved to be listed in the selected subnet when returning from node management screen in Matrix view
- #17862 Improved processing performance when deleting multiple sensors
- #17876 Improved problem that difficult to distinguish OS of agent action when node group condition is added


Bug Fixes
---------

- #17719 Agent down after trying macOS Agent Update
- #17911 Plugin does not work if period is specified for periodic execution of agent action
- #18003 api-ms-win-crt-runtime-l1-1-0.dll error when installing agent on a specific PC
- #18153 macOS agent and CWP display authentication status differently
- #17514 Fixed an issue where the alarm on the audit record filter for the new MAC detected does not work
- #17526 Fixed MatrixView tooltips that do not work properly
- #17558 Fixed the problem that the tooltip of macOS agent menu bar icon is broken
- #17640 Some monitor information may only be displayed when using multiple monitors
- #17650 When OTP code is generated in QR code for cloud, image is broken and security key reset button is not visible
- #17696 Fixed problem with 802.1x authentication due to EAP-GTC plugin unregistered on Windows
- #17776 Fixed the SNMP Write community string showing as always invalid
- #17818 Duplicate contents are sent to the same recipient when sending alarm by audit log filter
- #17868 There is a possibility that both devices can be maintained as Master when the policy server redundancy is configured
- #17926 Corrected time value incorrectly displayed among the collected antivirus information
- #18055 Invalid Agent Action permissions in Basic Edition fixed
- #18117 Fixed a problem where patch download fails if there are multiple interfaces of Policy Server or Distribution Server

.. _#17919: https://docs.genians.com/controlling/enforcement-methods.html#port-mirroring-span
.. _#16373: https://docs.genians.com/authentication/enabling-authentication/8021x.html?highlight=radius#authentication-using-radius-802-1x
.. _#17599: https://docs.genians.com/monitoring/managing-dashboards.html#managing-dashboards
.. _#17880: https://docs.genians.com/endpoints/network-interface.html?highlight=control%20network%20interface#controlling-network-interface
.. _#17663: https://docs.genians.com/endpoints/screen-lock.html?highlight=screen%20lock#controlling-screen-lock
