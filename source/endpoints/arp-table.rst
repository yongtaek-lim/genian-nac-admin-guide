Manage ARP Table
================

You can manage the ARP Table on the devices by Deleting Static ARP Entries, or preventing ARP conflicts

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Manage ARP Table** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Deleting Static ARP Entries**, turn **On** to delete static ARP entries
#. For **Static ARP for IP Conflict-prevention**, turn **On** to use Static ARP Entries for IP Conflict-prevention to prevent from ARP Spoofing 

   - **Node Group**, Optional setting to apply **Static ARP for IP Conflict-prevention** to specific Node Groups

#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Manage ARP Table** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

.. note:: Go to Management > Node > IPAM Tab > IP Policy to configure Conflict-prevention Settings
