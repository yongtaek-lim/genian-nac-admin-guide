Manage ARP Table
================

You can manage the ARP Table on the devices by Deleting Static ARP Entries, or preventing ARP conflicts

To See the Configuration of the Plugin
--------------------------------------

- Go to **System > Update > Genian Software > Plugin > Manage ARP Table**

Add the Agent Action to a Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Manage ARP Table** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Manage ARP Table
----------------

You can manage the ARP Table on the devices by Deleting Static ARP Entries, or preventing ARP conflicts

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Manage ARP Table** in the Agent Action window
#. Enter in **Conditions**, optional conditions for specific Criteria

Under **Settings**

#. For **Deleting Static ARP Entries**, turn **On** to delete static ARP entries
#. For **Static ARP for IP Conflict-prevention**, turn **On** to use Static ARP Entries for IP Conflict-prevention to prevent from ARP Spoofing 
#. For **Node Group**, Optional setting to apply **Static ARP for IP Conflict-prevention** to specific Node Groups
#. Click **Update**

.. note:: Go to Management > Node > IPAM Tab > IP Policy to configure Conflict-prevention Settings
