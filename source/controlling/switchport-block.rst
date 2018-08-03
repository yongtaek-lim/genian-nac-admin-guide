Configuring Switch Port Block
=============================

Configuring Switch Port Block for Enforcement Policies starts with the configuration of SNMP. By default, a read community string is configured,
but a write community string is needed to enforce switch port blocking.

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
---------------------------------------