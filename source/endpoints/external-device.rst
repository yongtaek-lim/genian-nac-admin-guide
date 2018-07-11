Controlling External Device
===========================

You can Control External Devices by disabling or uninstalling them and to force users to request for approval to use them for a set period of time. (External Devices can be any devices found within the Device Manager providing you know the Class Name and Vendor Name e.g. Class Name: "Universal Serial Bus controllers" Vendor Name: "USB Mass Storage Device")

To See The Configuration Of The Plugin
--------------------------------------

- Go to **System > Update > Genian Software > Plugin > Control External Device**

To Add The Agent Action To A Policy
-----------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control External Device** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

To Configure Control External Device Agent Action Settings
----------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control External Device**
#. Find **Agent Action** section and change settings as needed
#. Click **Update**

To Make The Agent Action Run Now
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click **Checkbox** of **Policy** to run
#. Click **Tasks > Run Action Now**

.. toctree::
   :maxdepth: 2

   externalusbstorage-policy
   externalusbprinters-policy
   