Port Scan Run
=========================

Genian NAC can detect port scanning run in a variety of ways. 
The Network Sensor monitors the network traffic flow to check the access event of ports.
If a port scan is run to find a virtual IP address in order to exploit a known vulnerability, Genians suspends the Port Scan Run and desinates the Node as a critical one.
In addition, if the ports are scanned more than the specified value within a period of time, then designated as a critical Node.


Step 1. Configure Threat Definition Settings for Port Scanning in Threat Definition
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Threat Definition** in the left Policy panel
#. Click **Port Scan**
#. Find **Threat Definition Settings** section
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

   - **ID**: "Port Scan Run", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **Port Scan**

#. Click **Update**
   
Step 3. Create Node Policy For Port Scanning
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "Port Scan Run", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **Port Scan Run Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** 
#. On **Threat** tab, select **Port Scan**
#. Click **Finish**