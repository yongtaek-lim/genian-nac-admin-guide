ARP Spoofing Sent
=========================

Genian NAC can detect any spoofed ARP packets sent  in a variety of ways. 
The Network Sensor listens for ARP replies on a network and checks of them whether there may be any changes or differences between the ARP sender MAC address and the Ethernet source MAC address.
If two responses are sent are different from each other, Genians suspends the ARP Spoofing Sent and designates the Node with the Ethernet source MAC address as a critical one. 
In addition, if the number of response packets allowed are more than the specified value, that Node is then designated as a critical one.

.. note:: If you use Virtual Router Redundancy Protocol (VRRP), the sender MAC address may differ from the Ethernet source MAC address, a real MAC address. Genian NAC discovers any cases of VRRP, HSRP or GLBP so that one of these cases will not be detected as a Threat.


Step 1. Configure Threat Definition Settings for ARP Spoofing in Threat Definition
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Threat Definition** in the left Policy panel
#. Click **ARP Spoofing**
#. Find **Threat Definition Settings** section
#. Specify **Event Duration**
#. Specify **Number of Allowable ARP Spoofing Packets** 
#. Click **Update**

Step 2. Create Status Group For ARP Spoofing Sent
----------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "ARP Spoofing Sent", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **ARP Spoofing**

#. Click **Update**
   
Step 3. Create Node Policy For ARP Spoofing
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "ARP Spoofing Sent", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **ARP Spoofing Sent Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** 
#. On **Threat** tab, select **ARP Spoofing**
#. Click **Finish**