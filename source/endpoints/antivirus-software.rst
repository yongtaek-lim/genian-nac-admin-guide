Controlling Antivirus Software
==============================

Policy Server communicates with the Agent to collect information on the Antivirus Software installed on end users Windows devices so you can  control scans, and force updates.

List of Supported Antivirus by Version
--------------------------------------

See all Antivirus supported with Genian NAC by version.

+---------------+--------------------------------+---------------+
|Vendor         |Product                         |Genian Version |
+===============+================================+===============+
|Ahnlab         |V3 Internet Security            |3.5.0          |
+---------------+--------------------------------+---------------+
|Avira          |Avira Antivirus                 |5.0.3          |  
+---------------+--------------------------------+---------------+
|BitDefender    |BitDefender                     |5.0.14         |
+---------------+--------------------------------+---------------+
|ESET           |ESET NOD32 ANTIVIRUS 9          |5.0.3          |
+---------------+--------------------------------+---------------+
|Estsecurity    |AIYak                           |3.5.0          |
+---------------+--------------------------------+---------------+
|Hauri          |ViRobot VRIS 2011, ViRobot 5.5  |3.5.0          |
+---------------+--------------------------------+---------------+
|Hauri          |ViRobot 7.0                     |3.5.0          |
+---------------+--------------------------------+---------------+
|INCA internet  |Anti-Virus/Spyware 3.0          |4.0.11/3.5.19  | 
+---------------+--------------------------------+---------------+
|Kaspersky      |Kaspersky                       |3.5.0          |
+---------------+--------------------------------+---------------+
|McAfee         |McAfee                          |4.0.23/3.5.19  |
+---------------+--------------------------------+---------------+
|Microsoft      |MS Forefront                    |4.0.7/3.5.1    |  
+---------------+--------------------------------+---------------+
|Microsoft      |MS Security Essentials          |5.0.3          | 
+---------------+--------------------------------+---------------+
|Microsoft      |MS System Center                |5.0.3          |  
+---------------+--------------------------------+---------------+
|Microsoft      |Windows Defender                |4.0.14         |  
+---------------+--------------------------------+---------------+
|Symantec       |Norton Antivirus                |4.0.2/3.5.0    |
+---------------+--------------------------------+---------------+
|Trend Micro    |OfficeScan                      |3.5.0          |   
+---------------+--------------------------------+---------------+
|Virus Chaser   |Virus Chaser                    |4.0.2/3.5.0    | 
+---------------+--------------------------------+---------------+


To See the Configuration of the Plugin
--------------------------------------

- Go to **System > Update > Genian Software > Plugin > Control Antivirus Software**

To Add the Agent Action to a Policy
-----------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Antivirus Software** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

To Control Antivirus Software
-----------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Antivirus Software** in the Agent Action window
#. Enter in **CWP message**, **Conditions**, and adjust **Agent Actions** based off of your network requirements
#. Click **Update**
