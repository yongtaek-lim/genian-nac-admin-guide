Collecting Antivirus Software Information
=========================================

Policy Server communicates with the Agent to collect antivirus software information that is installed on your Windows devices

List of Supported Antivirus by Version
--------------------------------------

Check all Antivirus supported with Genian NAC by version.

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

Collect Antivirus Software Information
--------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect Antivirus Software Information** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Action** section

#. For **Boolean Operator**, leave as default **OR**
#. For **Settings**, leave the default and click **Add** button to include others if they are not listed
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action** section, click **Assign**
#. Find **Collect Antivirus Software Information** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

