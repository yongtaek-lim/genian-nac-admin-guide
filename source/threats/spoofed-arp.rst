Spoofed ARP
===========

Genian NAC can detect any spoofed ARP packets sent  in a variety of ways. 
The Network Sensor listens for ARP replies on a network and checks of them whether there may be any changes or differences between the ARP sender MAC address and the Ethernet source MAC address.
If two responses are sent are different from each other, Genians suspends the spoofed ARP packets sent and designates the Node with the Ethernet source MAC address as a critical one. 
In addition, if the number of response packets allowed are more than the specified value, that Node is then designated as a critical one.

.. note:: If you use Virtual Router Redundancy Protocol (VRRP), the sender MAC address may differ from the Ethernet source MAC address, a real MAC address. Genian NAC discovers any cases of VRRP, HSRP or GLBP so that one of these cases will not be detected as an Anomaly.


Step 1. Configure Settings for Spoofed ARP in Anomaly Definition
----------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Spoofed ARP**
#. Find **Anomaly Event** section to configure more options

   - For **Event Duration**, optional setting to specify how long the spoofed ARP response packets are sent:
   - For **Number of Allowable Spoofed ARP Responses**, optional setting to specify the threshold to trigger the anomaly detection

#. Click **Update**

Step 2. Create Status Group For Spoofed ARP Sent
------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. For **ID:** Spoofed ARP Sent
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For each **Anomaly** you want to add use the followings:

   - **Options:** Anomaly
   - **Operator:** Detected is one of
   - **Value:** Spoofed ARP

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**
   
Step 3. Detect Spoofed ARP Through Node Policy
----------------------------------------------

You may assign the Status Group of Spoofed ARP Sent you created in Step 2 into an existing Node Policy or create a dedicated Node Policy to detect **Spoofed ARP** pre-configured in Step 1. 
The anomaly, **Spoofed ARP**, detected through either an existing Node Policy or a new Node Policy will be seen a variety of ways, please see :doc:`/threats/detecting-threats`.

Step 4. Block Spoofed ARP Through Enforcement Policy
----------------------------------------------------

You may assign the Status Group of Spoofed ARP Sent you created in Step 2 into an existing Enforcement Policy or create a dedicated Enforcement Policy to block the Nodes with **Spoofed ARP** pre-configured in Step 1. 
Please see :doc:`/threats/blocking-threats`.