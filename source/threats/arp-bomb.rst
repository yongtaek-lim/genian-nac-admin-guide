ARP Bomb
========

Genian NAC can detect too many ARP request packets sent in a variety of ways. 
The Network Sensor counts how many ARP packets sent by each Node. 
If the ARP requests are sent more than the specified value, Genians suspects the ARP Bomb and designates the Node as a critical one. 


Step 1. Configure Settings for ARP Bomb in Anomaly Definition
-------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **ARP Bomb**
#. Find **Anomaly Event** section to configure more options

   - For **Event Duration**, optional setting to specify how long the ARP request packets are sent:
   - For **Number of Allowable ARP Requests**, optional setting to specify the threshold to trigger the anomaly detection
   - For **Attribute to Match**, optional setting to find a Node sending the excessive ARP packets

#. Click **Update**

Step 2. Create Status Group For ARP Packet Bombed
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** ARP Packet Bombed
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** ARP Bomb

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect ARP Bomb Through Node Policy
-------------------------------------------

You may assign the Status Group of ARP Packet Bombed you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **ARP Bomb** pre-configured in Step 1. 
The anomaly, **ARP Bomb**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block ARP Bomb Through Enforcement Policy
-------------------------------------------------

You may assign the Status Group of ARP Packet Bombed you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **ARP Bomb** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.