Preparing Network
=================

When planning your Genian NAC Deployment onto your network there are several considerations. 

- Where should the equipment be placed? 
- How will it connect to my switches?
- How many pieces of equipment do I need?
- What ports do I need to open for Genians to communicate?

Wired Connectivity
------------------

The Policy Server should be directly connected to your Core Switch port as an access port. 
The Network Sensor should be connected to an Edge Switch port that can be an access port, or trunk port.

Switches
--------

Switches can be Unmanaged or Managed when plugging in Genian NAC. Using 802.1q trunking for the Network Sensor 
requires a Managed Switch and each Network Sensor can handle up to 128 VLANs. 
Here is a suggested link to help with configuring your `Trunked Switch Port`_.

SNMP
----

Genians supports SNMP Version 1 and Version 2c. The read-only community string is used to check whether the node supports SNMP in the process of collecting information about the Node by the network sensor. If the node responds to an SNMP request, the sensor verifies that the node is a switch by verifying that it supports the BRIDGE-MIB through an SNMP query.
The read-write community string is used to make changes to the switches for port descriptions and shutting down switch ports.

WAN
---

If you have more then one location behind WAN Technologies then a Network Sensor would be required at each of these locations.

Wireless Connectivity
---------------------

Network Sensor with Wireless NIC is used to detect wireless packets and identify SSIDs that are both Internal to your network and External (Neighboring) to your network. Placement of the Network Sensor with Wireless NIC is critical as you do not want to place this in a Data closet where you will only detect Wireless SSIDs near the data closet. You will want to place the Network Sensor with Wireless NIC centrally to where you can detect the majority of the SSIDs around it.

Allowed Ports
-------------

+------------------+-------------------------------+--------------------------+--------------------+
|SRC IP            |DST IP                         |Service                   |Note                |
+==================+===============================+==========================+====================+
|                  |115.68.106.87, 1.241.151.0/24  |TCP/3898, 3899            |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|Policy Server IP  |(geniupdate.geninetworks.com)  |UDP/3898, 3899            |GENIAN Data SYNC    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |                               |TCP/37, 80, 443           |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|Policy Server IP  |115.68.106.86, 1.241.151.0/24  |TCP/80                    |MS Patch            |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |(winupdate.geninetworks.com)   |                          |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |                               |TCP/3870                  |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|Network Sensor IP |Policy Server IP               |UDP/3870, 3871            |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |                               |TCP/37, 80, 443           |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |                               |UDP/514                   |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |115.68.106.87, 1.241.151.0/24  |                          |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|Network Sensor IP |(winupdate.geninetworks.com)   |TCP/80                    |MS Patch file       |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |115.68.106.86, 1.241.151.0/24  |                          |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |(winupdate.geninetworks.com)   |                          |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|                  |                               |UDP/3870, 3871            |                    |
+------------------+-------------------------------+--------------------------+--------------------+
|PC IP (Agent)     |Policy Server IP               |TCP/80, 443, 8000, 3910   |                    |
+------------------+-------------------------------+--------------------------+--------------------+


.. note:: The above ports need to be open and accessible to allow the Policy Server to get weekly/monthly updates from the Genians Platform DB

.. _Trunked Switch Port: http://www.ciscopress.com/articles/article.asp?p=2181837&seqNum=7

