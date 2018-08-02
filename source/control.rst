Controlling Network Access
--------------------------

.. note:: This feature required Professional or Enterprise Edition

Based on the information collected through the network sensor and the agent, a policy can be established to restrict network use to the non-compliant device.

- **ARP Poisoning**: The Network Sensor can manipulate ARP packets to control access by intercepting and filtering all packets coming from unauthorized nodes.
- **802.1x (RADIUS)**: Genian NAC can act as a RADIUS Server to control 802.1x port access and MAC authentication.
- **DHCP**: Genian NAC can act as a DHCP Server allowing only authorized MAC Addresses to get an IP Address on the network.
- **Switch Port Shutdown**: Genian NAC can shutdown a Switch Port using SNMP when detecting an unauthorized node on the network.
- **Agent Action**: Agents provide Network Interface Shutdown, Wireless Connection Block, PC Shutdown and Notification plugins to help control devices directly.

.. toctree::
   :maxdepth: 1

   controlling/configuring-networksensor
   controlling/ipam-networkaccess
   controlling/nodegroup-networkaccess
   controlling/switchport-block