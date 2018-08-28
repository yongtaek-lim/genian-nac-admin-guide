Unknown Service Requested
=========================

Genian NAC can detect an unauthorized service requested in a variety of ways. 
The Network Sensor monitors the network traffic flow to check the access event of ports.
If an unwanted service is requested on any virtual IP addresses, Genians suspends the Unknown Service Request and desinates the Node as a critical one.
In addition, if the service requests are more than the specified value within a period of time, then designated as a critical Node.

Step 1. Configure Threat Definition Settings for Unknown Service Request in Threat Definition
-------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Threat Definition** in the left Policy panel
#. Click **Unknown Service Requested**
#. Find **Threat Definition Settings** section
#. Specify **Event Duration**
#. Specify **Number of Allowable Service Requests** 
#. Specify **Attribute to Match** to find a Node requesting an unauthorized service
#. Click **Update**

Step 2. Create Status Group For Unknown Service Requested
----------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Status Group**
#. Enter in the following:

   - **ID**: "Unknown Service Requested", Application Mode "Enable"
   - **Condition**: Criteria: **Threat**,   Operator: **Detected is one of**,   Value: **Unknown Service Request**

#. Click **Update**
   
Step 3. Create Node Policy For Unknown Service Request
----------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. Click **Next**
#. On **General** tab enter the following:

   - ID "Unknown Service Requested", Application Mode "Enable"

#. Click **Next**
#. On **Node Group** tab, select newly created Node Group **Unknown Service Requested Group**
#. Click Next**
#. On **Policy Preferences** tab, you may change some configuration settings if needed
#. Click **Next**
#. On **Agent Action** tab click **Next** 
#. On **Threat** tab, select **Unknown Service Request**
#. Click **Finish**