Software and Hardware Sizing
============================

Five ​steps ​to ​specifying ​the ​right ​software ​and ​hardware
----------------------------------------------------------------

This ​document ​provides ​a ​guideline ​for ​choosing ​the ​right ​Genian ​NAC ​software ​and ​hardware. ​Specifying ​the ​right ​software ​and ​hardware ​is ​dependent ​on ​a ​number ​of ​factors ​and ​involves
developing ​a ​usage ​profile ​for ​the ​users ​and ​the ​network ​environment. ​For ​best ​results ​we ​recommend
using ​the ​following ​step-by-step ​procedure:

  #. Find ​the ​“Total ​Active ​Devices”​ ​Number
  #. Find ​the ​“Total ​Active ​Nodes”​ ​Number
  #. Find ​the ​​“Total ​Managed ​Networks” ​Number
  #. Find ​the ​​“Total ​Agent ​Applied ​Devices”​ ​Number
  #. Check Availability ​and ​Reliability​ ​Requirements

Step 1. ​Identify ​the ​“Total ​Active ​Devices” ​Number for License
--------------------------------------------------------------------

The ​license ​of ​Genian ​NAC ​Software ​is ​based ​on ​the ​number ​of ​devices ​connected ​to ​the ​network ​and
running. ​The ​number ​of ​devices ​is ​measured ​by ​the ​number ​of ​unique ​MAC ​addresses ​connected ​to ​the
network. ​In ​order ​to ​purchase ​Genian ​NAC ​in ​the ​right ​size, ​it ​is ​necessary ​to ​know ​the ​number ​of ​devices ​in ​operation. ​This ​value ​can ​usually ​be ​found ​in ​the ​following ​ways:

   - The ​number ​recognized ​by ​the ​IT ​/ ​Network ​Administrator
   - The ​existing ​IT ​management ​system ​(Asset ​Mgmt, ​Network ​Monitoring)
   - Verifying ​actual ​numbers ​through `Genian NAC Trial Version`_ (Download and Identify Devices)

As your network grows, and the number of devices exceed your License limit, the information and logs of those devices will be hidden and cannot be used.
When devices are no longer seen on the network the License will then be carried over to the next active and running device.
If you purchase an on-premise product, there are no licensing deadlines, only maintenance expirations. If maintenance contract expires, 
then you cannot upgrade to a newer version or update any of the various databases.

Step 2. ​Identify ​the ​“Total ​Active ​Nodes” ​Number for Hardware
-------------------------------------------------------------------

You ​need ​to ​know ​the ​number ​of ​nodes ​to estimate ​the ​capacity ​of ​the ​policy ​server. ​A ​node ​is ​an ​endpoint ​on ​the ​network ​consisting ​of ​a
combination ​of ​IP ​and ​MAC. ​If ​a ​system ​with ​a ​single ​MAC ​address ​is ​using ​multiple ​IPs ​at ​the ​same ​time,
the ​number ​of ​devices ​is ​one, ​but ​the ​number ​of ​nodes ​can ​be ​several. ​Because ​Genian ​NAC ​manages
all ​information ​on ​a ​per-node ​basis, ​it ​is ​closely ​related ​to ​the ​number ​of ​nodes ​in ​the ​capacity ​of ​the
policy ​server.

Depending ​on ​the ​number ​of ​nodes ​in ​the ​network ​you ​wish ​to ​install, ​we ​recommend ​the ​following
minimum ​specifications ​for ​policy ​server:

+-----------+----------------------+--------------------------+---------------------------+
|           |2,000 Nodes           |10,000 Nodes              |20,000 Nodes               |
+===========+======================+==========================+===========================+
|CPU        |Intel Dual Core 2Ghz  |Intel E3 Quad Core 3.4Ghz |Intel E5 Quad Core 3.5GHz  |
+-----------+----------------------+--------------------------+---------------------------+
|Memory     |8 GB                  |16 GB                     |32 GB                      |
+-----------+----------------------+--------------------------+---------------------------+
|Storage    |SSD 128 GB            |SSD 256 GB                |SSD 512 GB                 |
+-----------+----------------------+--------------------------+---------------------------+

Step 3. ​Identify ​the ​“Total ​Managed ​Networks” ​Number
----------------------------------------------------------

Genian ​NAC ​requires ​the ​installation ​of ​a ​sensor ​for ​every ​single ​layer ​2 ​broadcast ​domain. ​Therefore,
the ​number ​of ​managed ​broadcast ​domains ​is ​an ​important ​factor ​in ​determining ​the ​sizing ​of ​the
product. ​The ​number ​of ​network ​sensors ​required ​depends ​on ​two ​factors:

 - Number ​of ​VLANs
 - Number ​of ​remote ​networks ​with ​routing

A ​single ​network ​sensor ​can ​support ​up ​to ​128 ​VLANs. ​When ​an ​802.1Q ​VLAN ​Trunk ​connection ​is
provided ​through ​the ​Core ​Switch, ​sensor ​services ​for ​up ​to ​128 ​networks ​are ​provided ​over ​a ​single
physical ​connection. ​If ​the ​managed ​network ​is ​physically ​separated ​and ​configured ​as ​a ​WAN
connection, ​one ​Sensor ​will ​not ​be ​able ​to ​configure ​Layer ​2 ​connections ​to ​different ​regions. ​If ​this ​is
the ​case, ​you ​will ​need ​to ​configure ​a ​separate ​sensor ​for ​the ​remote ​network.

For ​example, ​if ​you ​have ​a ​corporate ​network ​with ​60 ​VLANs ​and ​two ​branch ​offices ​with ​3 ​VLANs ​each,
you ​will ​need ​a ​total ​of ​three ​sensors.

Step 4. ​Identify ​the ​“Total Agent ​Applied ​Devices” ​Number
---------------------------------------------------------------

The ​number ​of ​systems ​requiring ​agent ​installation ​is ​closely ​related ​to ​the ​capacity ​of ​the ​policy ​server.
Data ​and ​various ​events ​collected ​by ​the ​agent ​are ​sent ​directly ​to ​the ​policy ​server. ​Therefore, ​when ​the
number ​of ​agents ​is ​large ​or ​the ​agent ​performs ​complicated ​tasks, ​the ​load ​on ​the ​policy ​server
becomes ​high.
We ​recommend ​that ​you ​follow ​these ​minimum ​requirements:

+-----------+----------------------+--------------------------+---------------------------+
|           |1,000 Agents          |5,000 Agents              |10,000 Agents              |
+===========+======================+==========================+===========================+
|CPU        |Intel Dual Core 2Ghz  |Intel E3 Quad Core 3.4Ghz |Intel E5 Quad Core 3.5GHz  |
+-----------+----------------------+--------------------------+---------------------------+
|Memory     |8 GB                  |16 GB                     |32 GB                      |
+-----------+----------------------+--------------------------+---------------------------+
|Storage    |SSD 128 GB            |SSD 256 GB                |SSD 512 GB                 |
+-----------+----------------------+--------------------------+---------------------------+

Genian ​NAC ​supports ​agents ​for ​windows ​and ​macOS ​operating ​systems. ​The ​quantity ​of ​agents ​may ​be
less ​than ​or ​equal ​to ​the ​number ​of ​systems ​in ​which ​Windows ​and ​macOS ​operating ​systems ​are
installed.

The ​Genian ​NAC ​Policy ​Server ​can ​be ​divided ​into ​two ​parts: ​a ​node ​server ​that ​receives ​and ​processes
data ​from ​network ​sensors ​and ​agents, ​and ​a ​database ​that ​stores ​data. ​In ​a ​small ​to ​medium-sized
operating ​environment, ​it ​is ​common ​for ​two ​functions ​to ​work ​together ​on ​a ​single ​server, ​but ​in ​a
large-scale ​operating ​environment, ​the ​two ​functions ​can ​be ​operated ​as ​separate ​servers. ​If ​your 
network ​consists ​of ​more ​than ​10,000 ​nodes, ​consider ​configuring ​the ​node ​server ​and ​database separately.

Step 5. ​Availability ​and ​Reliability ​Requirements
-----------------------------------------------------

For ​availability ​and ​reliability, ​Genian ​NAC ​supports ​Active ​Standby ​configuration. ​By ​configuring ​Backup
system ​for ​policy ​server ​and ​network ​sensor, ​service ​can ​be ​provided ​without ​interruption ​in ​case ​of
master ​system ​failure. ​For ​this, ​Genian ​NAC ​provides ​its ​own ​HA ​capabilities ​to ​automatically ​detect
master ​system ​failures.

HA ​configuration ​requires ​an ​additional ​backup ​system ​for ​each ​system, ​so ​you ​need ​to ​prepare ​twice
the ​number ​of ​devices ​required ​for ​service ​configuration.

Sizing ​Questionnaire
---------------------

Please ​answer the ​following ​questions:

+--------------------------------------------+--------------------------------------------+
|Number of Devices                           |                                            |
|(Number of unique MACs on network)          |                                            |
+--------------------------------------------+--------------------------------------------+
|Number of Nodes                             |                                            |
|(Number of MAC+IP conbinations on network)  |                                            |
+--------------------------------------------+--------------------------------------------+
|Number of L2 Networks                       |                                            |
|(Number of broadcast domains)               |                                            |
+--------------------------------------------+--------------------------------------------+
|Number of Network Sensors                   |                                            |
|(One sensor supports up to 128 VLANs,       |                                            |
|each remote network needs a Sensor)         |                                            |
+--------------------------------------------+--------------------------------------------+
|Number of Agent Applied Devices             |                                            |
+--------------------------------------------+--------------------------------------------+
|Policy Server Functional Serparation        |  YES / NO                                  |
|(Node Server/Database Server)               |                                            |
+--------------------------------------------+--------------------------------------------+
|High Availability for Policy Server         |  YES / NO                                  |
+--------------------------------------------+--------------------------------------------+
|High Availability for Network Sensor        |  YES / NO                                  |
+--------------------------------------------+--------------------------------------------+

.. _Genian NAC Trial Version: https://www.genians.com/trial-buy/

