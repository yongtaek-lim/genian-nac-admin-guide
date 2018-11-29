Collecting Windows System Information using WMI
===============================================

Policy Server communicates with the Agent to use Windows Management Instrumentation (WMI) to obtain Windows system information on end users Windows devices

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Click **Tasks > Create** to create new Agent Action
#. For **Name**, type unique name (*e.g. WMI Identify Internal Battery*)

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**
#. For **Plugin**, select **Collect System Information Using WMI** from drop-down
#. For **Settings: Namespace**, select appropriate Namespace from drop-down or define Namespace in **User Defined Namespace** (*e.g. root\CIMV2*)
#. For **Settings: WMI Query**, type in optional queries separated by semicolon (*e.g. SELECT Caption FROM Win32_Battery*)
#. For **Execution Interval**, adjust Periodic Interval (*seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action** section, click **Assign**
#. Find and double click newly created **Agent Action** (*e.g. WMI Identify Internal Battery*)
#. Click **Add**
#. Click **Update**

See WMI Results
---------------

You can wait for the Policy to run on the defined schedule or you can Run Actions Now to see results immediately.

#. Click **Policy** in the top panel
#. Go to **Node Policy** in the left Policy panel
#. Click **Checkbox** of Default Policy
#. Click **Tasks > Run Actions Now** (*Wait a few minutes for this Action to run*)
#. Go to **Management > Node**, find and click on **IP** of Windows Node with Agent Installed
#. Find and click **System** tab
#. Find **WMI Status** section to view WMI results

Creating Status Group for WMI Results
-------------------------------------

Create Status Group based off of the WMI results from the **Agent Action** created from above. 
This Status Group then allows you to identify and enforce policies depending on your network requirements.

#. Click **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click **Tasks > Create New Status Group**

Under **General** section

#. For **Category**, Choose default or Create New (*This allows you to categorize your Node Groups*)
#. For **ID**, type unique name (*e.g. WMI Internal Battery Group*)
#. For **Description** (*Brief description of what this Node Group is for*)
#. For **Application Mode**, **Enabled**

Under **Condition** section

#. For **Boolean**, select "**AND**" or “**OR**” (*”AND” all conditions have to apply. “OR” any of the conditions have to apply*)
#. For **Settings**, click **Add** (*These are the various conditions to be applied for proper grouping*)
#. For **Options**, select **WMI**
#. For **Operator**, select appropriate option from drop-down (*e.g. class/property value are equal to*)
#. For **Value**,  type appropriate class/property value (*e.g. Win32_Battery/Caption, Internal Battery*)     
#. Click **Add**
#. Click **Save**

**WMI Query Examples:**

+--------------------------+-------------+------------------------------------------------------------------------------------------+
| WMI Name                 | Namespace   | WMI Query                                                                                |
+==========================+=============+==========================================================================================+
| Battery Info             | root\CIMV2  | SELECT Caption FROM Win32_Battery                                                        |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| HDD Vendor               | root\CIMV2  | SELECT Caption FROM Win32_DiskDrive                                                      |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| HDD Size                 | root\CIMV2  | SELECT Size FROM Win32_DiskDrive                                                         |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| HDD Model                | root\CIMV2  | SELECT Model FROM Win32_DiskDrive                                                        |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| HDD Serial               | root\CIMV2  | SELECT SerialNumber FROM Win32_DiskDrive                                                 |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| Volume Serial            | root\CIMV2  | SELECT VolumeSerialNumber FROM Win32_LogicalDisk                                         |
+--------------------------+-------------+------------------------------------------------------------------------------------------+ 
| Graphics Card Info       | root\CIMV2  | SELECT Caption, DriverVersion FROM Win32_DisplayConfiguration                            |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| Graphics Card Resolution | root\CIMV2  | SELECT CurrentHorizontalResolution, CurrentVerticalResolution FROM Win32_VideoController |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| HP Driver Version        | root\CIMV2  | SELECT * FROM Win32_PnPSignedDriver WHERE Devicename LIKE 'HP%'                          |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| NDIS Driver Version      | root\CIMV2  | SELECT * FROM Win32_PnPSignedDriver WHERE Devicename LIKE 'NDIS%'                        |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| Printer Info             | root\CIMV2  | SELECT Drivername FROM Win32_Printer                                                     |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| DHCP service             | root\CIMV2  | SELECT Description, DHCPEnabled, IPEnabled FROM Win32_NetworkAdapterConfiguration        |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| NIC Traffic Info         | root\CIMV2  | SELECT BytesSentPersec,BytesReceivedPersec FROM Win32_PerfRawData_Tcpip_NetworkInterface |
+--------------------------+-------------+------------------------------------------------------------------------------------------+

**WMI Status Group Examples:** (*Sample of the use of Operator: Equal to or Not Equal to, and Greater than or Less than*)

+------------------------+----------+--------------------------------------+-------------------------------------------+
| Status Group           | Options  | Operator                             | Value                                     |
+========================+==========+======================================+===========================================+
| WMI Internal Battery   | WMI      | class/property, value are equal to   | Win32_Battery/Caption, Internal Battery   |
+------------------------+----------+--------------------------------------+-------------------------------------------+
| WMI HDD Size           | WMI      | class/property, value are less then  | Win32_DiskDrive/Size, 536870912000        |
+------------------------+----------+--------------------------------------+-------------------------------------------+
