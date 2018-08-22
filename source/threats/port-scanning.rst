Port Scan Run
=========================

Genian NAC can detect port scanning run in a variety of ways. 
The Network Sensor monitors the network traffic flow to check the access event of ports.
If a port scan is run to find a virtual IP address in order to exploit a known vulnerability, Genians suspends the Port Scan Run and desinates the Node as a critical one.
In addition, if the ports are scanned more than the specified value within a period of time, then designated as a critical Node.


Step 1. Configure Anomaly Event Options for Port Scanning in Anomaly Definition
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly** in the left Policy panel
#. Click **Port Scanning**
#. Find **Anomaly Event** section
#. Specify **Event Duration**
#. Specify **Number of Allowable Ports** 
#. Specify **Attribute to Match** to find a Node running a Port Scan
#. Click **Update**

Step 2. Create Status Group For Port Scan Run
----------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "Port Scan Run", Status "Enabled"
   - **Condition**: Criteria: **Anomaly**,   Operator: **Detected is one of**,   Value: **Port Scanning**

#. Click **Update**
   
Step 3. Create Node Policy For Port Scanning
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "Port Scan Run", Status "Enabled"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **Port Scanning Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** 
#. On **Anomaly** tab, select **Port Scanning**
#. Click **Finish**