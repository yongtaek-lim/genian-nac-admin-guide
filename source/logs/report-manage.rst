Managing Reports
================

Query Report function, the Administrator can output the result of the query (SQL statement) desired by the 
Administrator as an Excel file in the report format. Query Reports define the report by setting up the query 
statement, and the report is created by the file creation operation on the defined report.

Generate Query Report
---------------------

#. Go to **Log > Report** in the top panel
#. Go to **Tasks > Generate Query Report**

Under **General**

#. For **Title**, type unique name
#. For **Description**, type what this report will do
#. For **Status**, select **Enabled**
#. For **Auto Generating**, select **Enable** for executing at set times

Under **Advanced**

#. For **File Format**, choose Excel or CSV from drop-down
#. For **Query**, add custom query

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

Generate Time Graph Report
--------------------------

#. Go to **Log > Report** in the top panel
#. Go to **Tasks > Generate Node Report**

Under **General**

#. For **Title**, type unique name
#. For **Description**, type what this report will do
#. For **Status**, select **Enabled**
#. For **Auto Generating**, select **Enable** for executing at set times

Under **Advanced**

.. note:: Repeat these steps under **Advanced** to add more **Node Options** to the report

#. For **Node Options**, select **All Nodes** or **Node Group** from drop-down
#. If **Node Group** is selected then for **Node Group** select desired group from drop-down
#. For **Criteria**, select what to report on
#. For **Name**, use default or type unique name
#. For **Description**, type what this report will do
#. For **Graph Type**, select **Line, Bar,** or **Face graph** from drop-down
#. For **Graph Color**, select desired color from drop-down
#. For **Generating Logs**, select desired criteria from drop-down
   
#. Click **Add** then **Update**
#. Go to **Report Definition > Click on newly created **Time Graph Report**

Under **Graph** tab

#. Select desired **Time Period** and click **Generate**

Under **Table** tab

#. Select desired **Time Period** and click **Generate**
#. Click **Export** to export report locally in **Excel** format

Create Automatic Reports
------------------------

.. note:: Automatic Report creation is the automatic generation and emailing portion of the Query Report. Email Account must be set up for Administrators

#. Go to **Log > Report** in the top panel
#. Go to **Automatic Report** in left **Report** panel
#. Go to **Tasks > Create** to create Automatic Report

Under **General**

#. For **Name**, type unique name
#. For **Description**, type what this report will do
#. For **Recipient**, select **Administrator** or **Admin Role**
#. Double click available names in left column
#. For **Report**, Double click available reports
#. For **Auto-generating**, select **Enable** from drop-down and choose how often to run this report
#. Click **Save**

Exporting Reports
-----------------

#. Go to **Log > Report** in the top panel
#. Go to **Report Definition**, click on desired **Report** name in left **Report** panel
#. Click **Tasks > Generate Report** (*File should appear to click on*)
#. Click on **Report Filename** to download (*e.g. 20180801110000.xlsx*)
#. Open **Report Filename** and save locally

How to Delete Reports
---------------------
 
#. Go to **Log > Report** in the top panel
#. Find **Report Definition** in the main window and click **Checkbox**
#. Go to **Tasks > Delete**
#. Click **OK** to verify deletion
