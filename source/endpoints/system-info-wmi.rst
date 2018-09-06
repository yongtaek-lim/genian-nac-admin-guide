Collecting Windows System Information using WMI
===============================================

Policy Server communicates with the Agent to use Windows Management Instrumentation (WMI) to obtain Windows system information on end users Windows devices

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect System Information Using WMI** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**
#. For **Namespace**, select appropriate Namespace from drop-down or define Namespace in **User Defined Namespace**
#. For **WMI Query**, enter in optional queries separated by semicolon
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect System Information Using WMI** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Creating Status Group for WMI Results
-------------------------------------

Create Status Group based off of the WMI results from the **Collect System Information Using WMI** plugin. 
These Status Groups then allow you to identify and enforce policies depending on your network requirements

#. Click **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click **Tasks > Create New Status Group**

Under **General**

#. For **Category**, Choose default or Create New (*This allows you to categorize your Node Groups*)
#. For **ID**, type unique name (*e.g. WMI Battery Info*)
#. For **Description** (*Brief description of what this Node Group is for*)
#. For **Application Mode**, **Enabled**

Under **Condition**

#. For **Boolean**, select "**AND**" or “**OR**” (*”AND” all conditions have to apply. “OR” any of the conditions have to apply*)
#. For **Settings**, click **Add** (*These are the various conditions to be applied for proper grouping*)
#. For **Options**, select **WMI**
#. For **Operator**, select appropriate option from drop-down (*Equal to or Not Equal to, Greater than, or Less than*)
#. For **Value**,  type appropriate class/property

   - Example Battery Info Setting: Option = WMI, Operator = class/property value are equal to, Value = Win32_Battery/Caption, Internal Battery

     
#. Click **Add**
#. Click **Update**

.. note: Results can be found in Node System View / WMI Status   MManagement > Node > Click IP of Node > System tab > Find WMI Status

Example: Identify Nodes having Internal Batteries Using WMI and Status Group
----------------------------------------------------------------------------

#. Go to **Policy > Node Policy > Agent Action**
#. Click **Tasks > Create**

Under **General** section

#. For **Name**, type **WMI Identify Internal Battery**

Under **Agent Actions** section

#. For **Plugin**, choose **Collect System Information Using WMI**   
#. For **Settings: Namespace**, select **root\CIMV2**
#. For **Settings: WMI Query**, enter **SELECT Caption FROM Win32_Battery**
#. For **Execution Interval**, select **In Periodic Interval**
#. Click **Update**
#. Go to **Policy > Node Policy** click on **Default Policy**
#. Find **Agent Action**. Click **Assign**
#. Find and double click **WMI Identify Internal Battery**
#. Click **Add**
#. Go to **Policy > Group > Node > Tasks > Create New Status Group**

Under **General** section

#. For **ID**, type **WMI Internal Battery Group**
#. For **Application Mode**, **Enabled**

Under **Condition** section

#. For **Boolean**, select **AND**
#. For **Settings**, click **Add**
#. For **Options**, select **WMI**
#. For **Operator**, select **class/property value are equal to**
#. For **Value**, select **Win32_Battery/Caption, Internal Battery**   
#. Click **Add**
#. Click **Apply**

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

+--------------------------+-------------+------------------------------------------------------------------------------------------+
| Status Group             | Boolean     | Condition                                                                                |
+==========================+=============+==========================================================================================+
| WMI Internal Battery     | AND         | WMI / class/property, value are equal to / Win32_Battery/Caption, Internal Battery       |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
| WMI HDD Size             | AND         | WMI / class/property, value are less then / Win32_DiskDrive/Size, 536870912000           |
+--------------------------+-------------+------------------------------------------------------------------------------------------+
