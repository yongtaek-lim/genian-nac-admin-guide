Detecting Threats
-----------------

A **Threat** may exploit vulnerabilities of a device, group of devices,  or to breach network security and therefore cause possible damage. A **Vulnerability** is an opening that can be exploited by threats to cause damage to a device, group of devices, or to network security.

Genian NAC inspects network traffic to identify abnormalities in the network and marks endpoint devices that have Threats. You can configure custom **Threat Definitions** or use the seven pre-defined definitions provided by default to detect endpoint devices that are exposed to major threats such as **Ad-Hoc Networks, ARP Bombing, ARP Spoofing, MAC+IP Clones,** and more.

- **Ad Hoc Network Connected**: Detects direct client-to-client communication
- **ARP Bomb**: Detects flooding of ARP requests
- **ARP Spoofing**: Detects spoofing of ARP Requests (Man-In-the-Middle)
- **Invalid Gateway Used**: Detects a node having an Invalid Gateway set
- **MAC / IP Clone**: Detects spoofing of IP/MAC Addresses
- **Port Scan**: Scans network for open ports to detect possible vulnerabilities
- **Unknown Service Requested**: Detects for Unknown Requested Services

.. toctree::
   :maxdepth: 2

   threats/understanding-threat
   threats/threat-definition
   threats/blocking-threats
   