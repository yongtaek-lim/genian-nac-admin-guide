MAC/IP Cloning
==============

Genian NAC can detect MAC / IP theft in a variety of ways. The Network Sensor periodically
sends an ARP request to check the operation status of Nodes. If two replies are received at the same
time, Genians suspends the MAC / IP clone and designates the Node as a critical Node. In addition, if the user
changes the MAC on the endpoint where the Agent is installed and the MAC is already being used by
another device, that device is then designated as a critical Node.
Genian NAC provides industry-leading platform detection to detect when a Node is changing
to another platform, allowing administrators to see when changes are made, and to block devices when
unauthorized platform changes are detected.


Step 1. Enable MAC/IP Clone on the Network Sensor
-------------------------------------------------

#. Go to **System** in the top panel
#. Go to **System > Sensor** in the left System Management panel
#. Click on **IP of Sensor** > **Settings** tab > click on **Sensor Settings**
#. Find **Node Status Scan: MAC+IP Clone Detection** section. Select **On** from drop-down
#. Click **Update**

Step 2. Create Status Group For MAC/IP Cloning
----------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "MAC/IP Cloning Group", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **MAC/IP Clone**

#. Click **Update**
   
Step 3. Create Enforcement Policy For MAC/IP Cloning
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Enforcement Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "MAC/IP Cloning", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab select newly created Node Group **MAC/IP Cloning Group**
#. Click Next
#. On **Permission** tab **double click** on **PERM-DNS**
#. Click **Next**
#. On **Redirection Action** tab click **Next**
#. On **Agent Action** tab click **Finish**
