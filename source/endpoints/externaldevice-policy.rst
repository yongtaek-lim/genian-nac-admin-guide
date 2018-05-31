Creating External Device Policy
===============================

You can create an External Device policy for an individual endpoint device.

To Add External Device For Device Policy
----------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name**
#. Find **Settings** section enter the following:

   - **Class Name**: “**Universal Serial Bus controllers**” found in Device Manager
   - **Name**: “**USB Mass Storage Device**” found in Device Manager

#. Click **Add**
#. Click **Save**

To Create External Device Policy
--------------------------------

(*Create Node Group for endpoint device that the External Device connects to using MAC Address for a condition. See Creating Node Groups*)

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action > External Device** in the left Policy panel
#. Click **Tasks > Create**
#. Find **General** section enter unique **ID name**. **Enable** the **Application Mode**
#. Find **Node Group** section. Click **Assign** to apply **Node Group**
#. Find **External Devices** section. Click **Assign** to apply newly created External Device group
#. Find **Exceptions** section. Click **Assign** to apply optional exceptions
#. Click **Save**
