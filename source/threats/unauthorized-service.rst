Unauthorized Service Request
============================

Genian NAC can detect an unauthorized service requested in a variety of ways. 
The Network Sensor monitors the network traffic flow to check the access event of ports.
If an unwanted service is requested on any virtual IP addresses, Genians suspends the Unknown Service Request and desinates the Node as a critical one.
In addition, if the service requests are more than the specified value within a period of time, then designated as a critical Node.


Step 1. Configure Settings for Unauthorized Service Request in Anomaly Definition
---------------------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Unauthorized Service Request**
#. Find **Anomaly Event** section to configure more options

   - For **Event Duration**, optional setting to specify how long the unauthorized services are requested:
   - For **Number of Allowable Service Requests**, optional setting to specify the threshold to trigger the anomaly detection
   - For **Attribute to Match**, optional setting to find a Node sending the excessive unauthorized service requests

#. Click **Update**

Step 2. Create Status Group For Unauthorized Service Requested
--------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Unauthorized Service Requested
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** Unauthorized Service Request

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect Unauthorized Service Request Through Node Policy
---------------------------------------------------------------

You may assign the Status Group of ARP Packet Bombed you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **Unauthorized Service Request** pre-configured in Step 1. 
The anomaly, **Unauthorized Service Request**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block Unauthorized Service Request Through Enforcement Policy
---------------------------------------------------------------------

You may assign the Status Group of Unauthorized Service Requested you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **Unauthorized Service Request** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.