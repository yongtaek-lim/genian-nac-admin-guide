Port Scanning
=============

Genian NAC can detect port scanning run in a variety of ways. 
The Network Sensor monitors the network traffic flow to check the access event of ports.
If a port scan is run to find a virtual IP address in order to exploit a known vulnerability, Genians suspends the Port Scan Run and desinates the Node as a critical one.
In addition, if the ports are scanned more than the specified value within a period of time, then designated as a critical Node.


Step 1. Configure Settings for Port Scanning in Anomaly Definition
------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Port Scan**
#. Find **Anomaly Event** section to configure more options

   - For **Event Duration**, optional setting to specify how long the port scan is run:
   - For **Number of Allowable Ports**, optional setting to specify the threshold to trigger the anomaly detection
   - For **Attribute to Match**, optional setting to find a Node running the port scan

#. Click **Update**

Step 2. Create Status Group For Port Scan Run
---------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Port Scan Run
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** Port Scanning

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect Port Scan Through Node Policy
--------------------------------------------

You may assign the Status Group of Port Scan Run you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **Port Scanning** pre-configured in Step 1. 
The anomaly, **Port Scanning**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block Port Scan Through Enforcement Policy
--------------------------------------------------

You may assign the Status Group of Port Scan Run you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **Port Scanning** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.