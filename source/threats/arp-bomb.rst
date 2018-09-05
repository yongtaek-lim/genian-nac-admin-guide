ARP Packet Bombed
=================

Genian NAC can detect too many ARP request packets sent  in a variety of ways. 
The Network Sensor counts how many ARP packets sent by each Node. 
If the ARP requests are sent more than the specified value, Genians suspends the ARP Bomb and designates the Node as a critical one. 


Step 1. Configure Threat Definition Settings for ARP Bomb in Threat Definition
------------------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Threat Definition** in the left Policy panel
#. Click **ARP Bomb**
#. Find **Threat Definition Settings** section
#. Specify **Event Duration**
#. Specify **Number of Allowable ARP Requests** 
#. Specify **Attribute to Match** to find a Node sending excessive ARP packets
#. Click **Update**

Step 2. Create Status Group For ARP Packet Bombed
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "ARP Packet Bombed", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **ARP Bomb**

#. Click **Update**
   
Step 3. Create Node Policy For ARP Bomb
---------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "ARP Packet Bombed", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **ARP Packet Bombed Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** 
#. On **Threat** tab, select **ARP Bomb**
#. Click **Finish**