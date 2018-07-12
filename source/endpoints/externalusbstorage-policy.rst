Creating External USB Storage Device Policy
===========================================

You can create an External USB Storage Device policy for Windows devices. This Policy can be used for External Hard Drives, Thumb Drives, or DVD Drives.

To Configure Control External Device Plugin
-------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control External Device**
#. Find **Agent Action > Control Methods** section and choose to **Disable** or **Uninstall**
#. Click **Update**
      
To Create External Device Group
-------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > External Device** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "USB Storage Devices"*)
#. Find **Settings** section enter the following:

   - **Class Name**: “**Some-Name**” found in Device Manager (*e.g. Universal Serial Bus controllers*)
   - **Name**: “**Some-Vendor-Name**” found in Device Manager Details (*e.g. USB Mass Storage Device*)

#. Click **Add**
#. Click **Save**

   
**For USB External Storage Devices**

   - **Class Name**: “**Universal Serial Bus controllers**” found in Device Manager
   - **Name**: “**USB Mass Storage Device**” found in Device Manager
   
   AND
   - **Class Name**: “**Storage controllers**” found in Device Manager
   - **Name**: “**USB Attached SCSI (UAS) Mass Storage Device**” found in Device Manager   
   
**For External DVD Drives** 
 
   - **Class Name**: “**DVD/CD-ROM drives**” found in Device Manager
   - **Name**: “**Some Vendor Name**” found in Device Manager 
   
(*You can build Policies to Identify and Disable anything found in the Device Manager with Proper Class Name and Vendor Name*)   
 
To Create External Device Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action > External Device** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "USB Storage Policy"*)
#. Find **Node Group** section click **Assign** and choose **Node Group**
#. Find **External Devices** section click **Assign** and choose **USB Storage Devices**
#. Click **Update**
#. Click **Apply**

To Create Node Policy for External Device Policy
------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "Node Policy for USB Storage Devices"*)
#. Find **Node Group** section click **Assign** and choose **Node Group**
#. Find **Agent Action** section click **Assign** and choose **Control External Device**
#. Click **Update**
#. Click **Apply**


To Run Agent Actions Now
------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click Checkbox of **Policy** (*e.g. "Node Policy for USB Storage Devices"*)
#. Click **Tasks > Run Actions Now**

