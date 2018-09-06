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
#. For **Namespace**, select appropriate namespace from drop-down or define namespace in **User Defined Namespace**
#. For **WMI Query**, enter in optional queries separated by semicolon
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect System Information Using WMI** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

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
