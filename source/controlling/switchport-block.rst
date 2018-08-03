Configuring Switch Port Block
=============================

Configuring Switch Port Block for Enforcement Policies starts with the configuration of SNMP. In order to block the ports of the switch
to which the node is connected, Genian NAC needs the information of the switch port to which the node is connected. This is accomplished
by reading the switch port information through a switch that supports SNMP.

The read community string is used to check whether the node supports SNMP in the process of collecting information about the node by
the network sensor. If the node responds to an SNMP request, the sensor verifies that the node is a switch by verifying that
it supports the BRIDGE-MIB through an SNMP query.

To Configure SNMP Read Community String
---------------------------------------

#. Click **Preferences** in the top panel
#. Go to **General > Node** in the left panel

Under **SNMP**

#. For **SNMP Community**, type your switches read community strings. (separated by comma if you have multiple community string)
#. For **Collecting Network Information**, select **On**
#. For **Scanning Interval**, select desired switch port information update interval
#. For **Time Object**, select the desired time object if you want information collection to work only at a specific time
#. For **Scan Now**, click the button if you want to collect information immediately (MUST click Update button first if you changed settings)
#. Click **Update**

To Configure SNMP Write Community String
----------------------------------------

Actual switch port blocking is done via SNMP write. The switch MUST provide a writable SNMP MIB-2 ifAdminStatus property.
To do this, you must set the switch's write community as follows:

#. Click **Management > Switch** in the top panel
#. Click **Switches** in the left panel
#. Click desired switch's **Switch Name** column
#. For **Write Community**, enter this switch's write community string
#. Click **Update**

Enable Switch Port Shutdown on Enforcement Policy
-------------------------------------------------

The target of the switch port blocking is determined by the Enforcement Policy. If you want to block switch ports for specific nodes,
you need to create an enforcement policy that targets those nodes and then configure the switch port blocking setting.