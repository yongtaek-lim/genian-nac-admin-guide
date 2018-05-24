Managing Reports
================

Query Report function, the Administrator can output the result of the query (SQL statement) desired by the 
Administrator as an Excel file in the report format. Query Reports define the report by setting up the query 
statement, and the report is created by the file creation operation on the defined report.

How to Generate Query Report
----------------------------

#. Go to **Log > Report** in the top panel
#. Go to **Tasks > Generate Query Report**
#. Find **General** section and enter the following:

   - Title
   - Description
   - Application Mode: Enable
   - Auto-generating: (*Disabled by default, but enable if you want to schedule report periodically*)

#. Find **Policy Preferences** section and enter the following:

   - File Type
   - Query

#. Click **Save**

Example Queries
---------------

Collect Open Ports Of Nodes
```````````````````````````

.. code:: sql

 SELECT NL_IPSTR as IP, NL_MAC as MAC, NL_FQDN as HOSTNAME, GROUP_CONCAT(NI_PORT) as OPENPORT
   from vwNODELIST_ALL JOIN NODEINFOALL_OPENPORT ON (NI_NODEID = NL_NODEID)
   where NL_ACTIVE = ‘1’
   GROUP BY NL_NODEID
   
List Of IPs With The Same MAC
`````````````````````````````

.. code:: sql

 SELECT * FROM (
   SELECT NL_IPSTR, COUNT(NL_MAC) CNT
     from vwNODELIST_VALID
     GROUP BY NL_IP
     ORDER BY NL_IP
 ) A WHERE CNT > 1

 The Administrator uses the Time Graph Report to show the information about the Node Group and the whole Node, 
 the operation, the Agent installation, and the number of operation Agent Nodes in a Graph Format.

How to Generate Time Graph Report
---------------------------------

#. Go to **Log > Report** in the top panel
#. Go to **Tasks > Generate Query Report**
#. Find **General** section and enter the following:

   - Title
   - Description
   - Application Mode: Enable
   - Auto-generating: Enable (*Choose the reoccurring frequency*)

#. Find **Policy Preferences** section and enter the following:

   - Data Source (*All Nodes, Node Group*)
   - Criteria (*All Nodes, Nodes Up, Nodes with Agent Installed, Nodes with Agent Running*)
   - Name
   - Description
   - Graph Type (*Line Graph, Bar Graph, Face Graph*)
   - Graph Color
   - Generating Logs Threshold
   
#. Click **Add** then **Save**

Automatic Report creation is the automatic generation and emailing portion of the Query Report.


How to Create Automatic Reports
-------------------------------

(*Email Account must be set up for Administrators*)

#. Go to **Log > Report** in the top panel
#. Go to **Automatic Report** in left **Report** panel
#. Go to **Tasks > Create** to create Automatic Report
#. Find **General** section and enter the following:

   - Name
   - Description
   - Recipient
   - Report (*Report Definition created above*)
   - Auto-generating (*Choose how often this report runs*)

#. Click **Save**

How to Delete Reports
---------------------
 
#. Go to **Log > Report** in the top panel
#. Find **Report Definition** in the main window and click **Checkbox**
#. Go to **Tasks > Delete**
#. Click **OK** to verify deletion