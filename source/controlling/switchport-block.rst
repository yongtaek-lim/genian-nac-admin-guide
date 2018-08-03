Configuring Switch Port Block
=============================

Configuring Switch Port Block for Enforcement Policies starts with the configuration of SNMP. By default, a read community string is configured,
but a write community string is needed to enforce switch port blocking.

To Configure SNMP Read Community String
---------------------------------------

#. Click **Preferences** in the top panel
#. Go to **General > Node** in the left panel
#. Find **SNMP** section. Enter the following:

   - **SNMP Community** (*’public‘ for read, ‘public,private‘ for read-write*)
   - **Collecting Network Information** (*On*)
   - **Scanning Interval** (*5min.-1year (Suggest starting off with once a day*))
   - **Time Group**

#. Click **Scan Now**

