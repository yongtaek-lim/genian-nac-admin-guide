Understanding Genian NAC
========================

Genian NAC consists of 3 primary processes:

  - **Visibility** – Collecting, analyzing, and categorizing everything on the network.
  - **Compliance** – Assessing the current security practices and reshaping policies to ensure endpoints are in compliance with the IT security policies.
  - **Control** – Manipulating endpoint’s system configuration, maintaining your IT security baseline, enforcing policy compliance manually or automatically to ensure the safety of the network, users, and data.

Visibility
----------

Once Genian NAC is deployed, visibility is the initial objective. It is important to collect as much information as possible about every Node on the network.

**Node**

A Node is a general term to describe any type of device with network interfaces to access the network. Essentially, each network interface is a Node. Each Node corresponds to the IP address with the MAC address of the device attempting to connect to the network. Often, a device has multiple MAC addresses, such as a switch, server or laptop with Ethernet and Wireless network interface cards (NIC). This means that this laptop (host) is associated with more than one Node network interface.

**Group**

A group provides a way to categorize common things and makes it easier to perform tasks on the group rather than on each individual item. For example, a Node group is a collection of Nodes with some common feature. For example, the All Nodes Group is a container of all Nodes. Nodes groups can be used for a variety of purposes, such as with a Policy, Report, or Dashboard Widget. Think logically when setting up your groups.

**Platform and Node Type**

The Genian NAC Policy Server detects the platform information of the connecting device (host) and compares it against the Genian NAC database, which has over 40,000 Device Platform definitions. Geni Networks’ engineers add new or updated definitions as they become available to the Genian Cloud, from which they can be downloaded to your local Genian NAC Policy Server. Whenever, there is incorrect or missing platform information, you can request a fix through the Genian NAC Admin Web UI.

The platform is further classified as one of the defined Node Types (such as Router, Switch, Server, Security devices, PC, Mobile devices, Printer and more) making it easier to locate and add them to appropriate Node groups. By default, it provides 12 different types of Nodes and you can even create your own Node Type. Categorizing Nodes Types can enhance visibility.

The more of Node information Genian NAC collects, the better you can make decisions to protect your network environment. Genian NAC dives into gaining information “granularity”. By adding more and more details about each Node, the resultant Genian NAC makes the network transparent to see all activity crystal clear.

Once the Sensors and Agent receives policies from the Policy Server, they run the policies independently by their own intelligence, reporting back to the Policy Server only when the Node security posture has changed.

**Visibility, plus more**

The Admin Web User Interface can be customized for your specific monitoring and management needs. For instance, you can set up your own widgets for condition-based Node groups, and you can even create role-based Admin user accounts for personalized dashboard views.

Additionally, Genian NAC can provide Geo-based Critical Event monitoring by the Sensors. Basically, an intuitive geographic interface powered by Google Maps allows you to monitor the Network Security Status of your network in a specific country region, state/province or city. The condition of a Node group can be visually monitored in real-time. You can zoom in for specific details or zoom out for an aggregated data view.

Network Visibility
******************

Before deploying Genian NAC to your network, you may have had an idea of what is on the network, based on your IT lists of company assets. However, it is probable that you will not know about all of the other devices connected to the network. Your asset list is likely to be out-of-date. This is often true when there is a shortage of IT resources to maintain documentation as resources are moved, updated, or removed (End of Life).

Turning on the Genian NAC Policy Server with the Network and Wireless Sensor illuminates the entire network, exposing whatever is there and presents the collected data in the Web UI views. You can sort and filter the associated data.

User Visibility
***************

To know your users as well as inform them about your network security policies, you need to first identify who they are, and then continue to manage those users.

To identify users, Genian NAC Policy Server authenticates the user using the following methods:

  - 802.1x EAP and RADIUS
  - User Database Synchronization: Synchronized with an existing user database such as LDAP, Oracle, MySQL, MS SQL/Sybase, DB2, CSV. It can be saved in Genian NAC DB.
  - External Database Integration: The Policy Server can also be integrated with third-party user management standards with direct access to user information, such as LDAP, POP3/IMAP, NextGen Firewall (PaloAlto).
  - Captive Web portal: Genian NAC provides an onboarding process with user agreement and registration forms.)

Once a new user is identified, he or she is automatically associated with the user’s device (refer to “Endpoint Visibility”).

User identity and behavior is important to the outcome of your security strategy. Users who are ignorant of the importance of security and the reasons for maintaining a healthy device for your network environment will unwittingly carry malicious threats to your internal network. Not only will an informed user have better computing performance because of complying with your security policies, but will be a good member of the network community.

Endpoint Visibility
*******************

The Network and Wireless Sensors collect such information about endpoint devices as platform type (e.g., laptop, smartphone, tablet), address (IP/MAC), vendor, connected switch port, services (Web, DNS, NAT, AP), and abnormal traffic. The authentication process collects and verifies information about the device’s user. But you still do not have the detailed information about what is inside of the company-owned devices and what has been changed by authenticated users.

To gather the endpoint’s system information thoroughly, you must install the Agent on the endpoint.

**Agent**

The Agent is installed directly on the endpoint device to manage what is on the endpoint device itself. This is crucial to granular information about the endpoint that cannot be collected otherwise by the Network and Wireless Sensor.

Most other vendor agents scan and manage endpoint information by running a scheduled task that attempts to gather and manage all information from all endpoints at one time. This is extremely inefficient. This process requires a lot of resources (Network Bandwidth, CPU Cycles, and Memory consumption) between endpoints and the managing servers.

The Genian’s Agent does more than just typical scanning and remediation and performs its tasks more efficiently by communicating with the Policy Server only when events set by your policy requirement occurs, without interrupting system or network performance. The Agent also provides Desktop Management capabilities, Application Management (add/remove software), OS Configuration, OS Patch Management, Peripheral Device Management, and Wireless Connection Management.

The Agent manages the endpoint system information, such as the operating system, patches, applications, registry entries, and services, that aids you in detecting and dealing with potentially dangerous malware strings and scripts lurking on the endpoint, which could easily threaten your network, data, and system processes. That is why it is so important to gain visibility into each endpoint devices – not to prevent a user from using the device, but for maintaining the safety and performance of your network from IT asset management perspective. Users should appreciate this because they will also be protecting their valuable personal data.

The Genian NAC Policy Server matches this data collected by the Agent to the Node policy with which the endpoint is associated to determine its compliance status (refer to “Compliance”).

Compliance
----------

The primary objective of setting up your compliance requirements is to assess your current IT security practices, discover the security status of all endpoints on the network, and align them all to your IT security baseline. Thereafter, it will be easier to catch non-compliant endpoints connecting to your internal network, as well as make changes to your security strategy when it becomes necessary. One or two unknown, non-compliant devices may not be an issue, which is easily remedied. However, if more than 10% of the Nodes are unknown, or organization-owned devices are not compliant, you may have some headaches to manage the situation.

With Genian NAC, you can fix your IT security practices effectively by setting up the Node groups, Policies, Actions, and Permissions that will define security compliance for your network environment.

Node Groups
***********

To simplify the process of setting up your security baseline, you will work with Nodes and Policies, which define specific conditions that must be met to be “in compliance”. There are two groups that define what you are controlling:

**Policy Group**

Group based on Node-related information such as Node type, address information (IP/MAC), user information (authentication), accessing time, and more.

**Status Group**

Group based on the Node status measured by policies and the associated conditions.

Both groups can be used to assess the current security practices in your organization. A status group can be used to enforce policy on non-compliant Nodes (refer to “Access Control”).

Grouping Nodes provides significant administrative benefits by simplifying tasks, organizing resources, and applying policies dynamically across the network. When you need to make changes affecting every Node in a group, it is easier to modify the settings for the Node group.

Policies, Actions, and Permissions
**********************************

Once a targeted Node group is ready, you can set up specific policies with appropriate actions and permissions.

**Policy**

Define a security policy that describes how to secure access to Nodes when endpoints attempt to access your internal network. There are four types of policies:

  - Node Policy: Secure endpoints (authentication and system management) using Agent plugins.
  - Enforcement Policy: Manage secure access control using the Sensors and Agent.
  - WLAN Policy: Enable the AP feature in the Wireless Sensor.
  - Compliance Policy: Apply a Node to multiple Node groups so you can easily identify the overall Node status of compliance defined by the Node groups. This kind of policy setup process can support various regulatory compliances, such as PCI, HIPAA, FERPA, more dynamically and effectively.

**Action**

Policies can be executed by Actions. Various Actions can be supported by Agent plugins. (By default, 32 plugins are available to Node policies and 3 plugins to enforcement policies.)

**Permission**

To apply policies more accurately, you need to specify a scope with 3 different objects: Network, Service and Time.

  - Network: A range of IP address, network segments (IP netmasking)
  - Service: Transport and Network layer protocols (TCP, UDP, ICMP)
  - Time: A range of Date, Days, Times

To define what the policy compliance will be for your internal network, you need to set up the Node Policy that users and their devices must follow, and then apply these policies to the targeted Node groups so you can identify which endpoints are currently not in compliance.

For example, you may want to ensure that all organization-owned endpoint devices running Windows OS must have the Agent and the required Anti-Virus software must be installed. To achieve the goal, you can create a Node policy and assign the policy to “Agent Is Installed” Node Group (which is set up for all Nodes that are supposed have the Agent), and “Antivirus Not Installed” Node Group (which is set up for any Nodes that does not have Antivirus).

After deciding on the targeted Node groups, you can apply the appropriate Actions (Collect OS and Software Information, Check a specific Antivirus Information) and Permission (e.g., only scans employee network segment between 8 AM to 5PM) to the Node groups.

Once the Node policy is turned on, you can immediately see those devices that are not in compliance with the policy. From this baseline, you can determine what to do with those non-compliant devices.

Preventing network access by non-compliant requires the Enforcement Policy. This Policy is referred to as “Control”, which often entails preventing access until endpoints remediates the non-compliance issues (refer to “Endpoint Control”).

Audit and Report
****************

Genian NAC gathers event information for the entire network from the Sensors and Agent. And it stores it in Genian NAC database. All Network and Agent events along with historical data can be logged into Genian NAC database and you can easily find out a specific event data by filters and full-text search. The log data can be integrated with any Next Generation Firewall, APT, and SIEM solutions. You can generate customized reports by Excel format or graphic chart based upon schedule basis.

Control
-------

Once the IT Security Baseline has been established, Genian NAC Policy Server with Sensors and Agent is positioned to enforce compliance with your IT security policies.

Network Access Control
**********************

There are a variety of enforcement and control options available, such as using Address Resolution Protocol (ARP) poisoning, Port mirroring, or TCP/IP connection reset:

  - Protocol Control: ARP, DHCP, TCP/IP, ACL, SNMP
  - Switch Port Control: Port mirroring
  - Endpoints Access Control: Captive Web Portal and Agent.

  Each control option essentially prevents access to your internal network unless the user follows directions to remediate the endpoint devices to be compliant.

The Enforcement Policy can be integrated with third-party security solutions such as a Next-generation Firewall, IDS/IPS, to receive Syslog messages about potential threat events. When an endpoint triggers such a critical security event, the integrated security device forwards the event message to the Genian NAC Policy Server, which marks the endpoint as out-of-compliance. What happens thereafter depends on the actions set up in the Node and Enforcement policies for that endpoint.

**Node Control**

You can list all discovered Node (or device) information and directly apply Policies related to IP/MAC, Authentication, and Hostname to selected Node(s) or device(s). You can also add a Node(s) to certain Node group(s).

**Switch Port Control**

Using 802.1x port based access control, Genian NAC Policy Server with Network Sensor can shut down any ports connected by non-compliant devices.

**IP Address Control**

Provisioning IP addresses is critical to manage all types of Nodes more efficiently. So you should be able to plan, monitor, and control IP address usage dynamically.

  - Force endpoints to use only specific IPs
  - Change an incoming IP address to another IP
  - Prevent IP conflicts
  - Apply an IP reservation process to reserve an IP address (If a non-authorized user tries to use that IP to access the network, the access is denied.)
  - Apply Node policy to IP address directly.

  Genian NAC Policy Server can support all tasks mentioned above through the intuitive matrix interface and it can be integrated with DHCP server to monitor and manage the IP usage. (The built-in DHCP service in the Genian NAC Policy Server is also available.) Most important, IP addresses should be allocated to only compliant devices right-on-time, and all historical access logs of IPs should be saved to support regulatory compliance.

**WLAN Control**

With so many Wifi-enabled devices accessing through APs, it is important to detect which APs belong to your internal network or not. Also, it is important to guide users to use verified APs only. You can allow or deny Wifi-enabled devices accessing different SSIDs based on the policy compliance by Node groups, such as Authorized AP, Rogue AP, Misconfigured AP, Tethering device, and more.

**User Control**

You can control user information, such as role, password, activation, IP/MAC information, basic contact information.

Endpoint Control
****************

The endpoint is the ultimate threat to the safety and security of the internal network. Geni Networks recognizes the importance of the end user experience when accessing the network environment. As a consequence, the Agent communicating with the Genian NAC Policy Server manipulates endpoint devices through two possible ways: Configuration Management or User Awareness.

  - Configuration Management: This method is performed without users being involved in the decision. Often this technique is used for the initial deployment of the NAC solution with Node policy.
  - User Awareness: Users are involved in the decision of the access to the network. It can be communicated through various communication methods, such as Captive Web Portal, SNS, email, and Popup message by the Agent.

  Both methods require the Agent. Basically, the Agent installed on endpoint devices communicates with the Genian NAC Policy Server directly to monitor policy compliance and, as necessary, control. Through the Agent, Genian NAC Policy Server provides notification messages to the endpoints, as well as the appropriate stakeholders (for example, Administrators).

The Agent can control the endpoint’s system configurations such as Network Interface Card (NIC) and Power. For example, an enforcement policy can be set up to shut off the NIC or just power off the device immediately when one of its assigned devices is detected as a source of a possible threat. Additional control options include:

  - Application management: Force to install/remove software
  - Operating System configuration: Control Registry
  - Operating System Patch management: Force to install Patches.
  - External Device control: Block USB storage, printer access, DVD-RW
  - Wireless Connection Management: Provide a single-click wireless connection service.

Since network security is so dependent on user behavior and knowledge, the best practice over the operational life of the NAC solution is the User Awareness method. By setting up Node and Enforcement policies for an “Awareness” compliance program, whereby the user is informed about their non-compliant behavior with instructions how to remedy their condition, they can learn how and why to be compliant, and have an improved user experience in using the network.

