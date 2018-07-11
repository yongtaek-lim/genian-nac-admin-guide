Creating External USB Printer Policy
====================================

To Configure Control External Device Plugin
-------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control External Device**
#. Find **Agent Action > Control Methods** section and choose to **Disable** or **Uninstall**
#. Click **Update**
      
Create External Device Group
----------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > External Device** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "USB Printers"*)
#. Find **Settings** section enter the following:

   - **Class Name**: “**Printers**” found in Device Manager
   - **Name**: “**Some-Vendor-Name**” found in Device Manager Details

#. Click **Add**
#. Click **Save**
   
(*You can build Policies to Identify and Disable anything found in the Device Manager with Proper Class Name and Vendor Name*)   
 
Create External Device Policy
-----------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action > External Device** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "External USB Printer Policy"*)
#. Find **Node Group** section click **Assign** and choose **Node Group**
#. Find **External Devices** section click **Assign** and choose **USB Printers**
#. Click **Update**
#. Click **Apply**

Create Node Policy for External Device Policy
---------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name** (*e.g. "Node Policy for USB Printers"*)
#. Find **Node Group** section click **Assign** and choose **Node Group**
#. Find **Agent Action** section click **Assign** and choose **Control External Device**
#. Click **Update**
#. Click **Apply** 

To Run Agent Actions Now
------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click Checkbox of **Policy** (*e.g. "Node Policy for USB Printers"*)
#. Click **Tasks > Run Actions Now**
