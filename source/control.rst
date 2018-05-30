Controlling Network Access
--------------------------

To control network access, you can use a Node Group, which can be enforced by 5 different methods:

- **ARP Poisoning**: The Network Sensor can manipulate ARP packets to control access by intercepting and filtering all packets coming from unauthorized nodes.
- **802.1x (RADIUS)**: Genian NAC can act as a RADIUS Server to control 802.1x port access and MAC authentication.
- **DHCP**: Genian NAC can act as a DHCP Server allowing only authorized MAC Addresses to get an IP Address on the network.
- **Switch Port Shutdown**: Genian NAC can shutdown a Switch Port using SNMP when detecting an unauthorized node on the network.
- **Agent Action**: Agents provide Network Interface Shutdown, Wireless Connection Block, PC Shutdown and Notification plugins to help control devices directly.

.. toctree::
   :maxdepth: 2

   controlling/configuring-networksensor
   controlling/ipam-networkaccess
   controlling/nodegroup-networkaccess
   controlling/switchport-block