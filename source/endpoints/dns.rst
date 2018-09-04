Controlling DNS
===============

You can control DNS to obtain DNS automatically or assign DNS manually to point to a specific DNS server.
You can also add and remove entries within the devices Host File

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control DNS** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**
#. For **DNS Configuration**, select to obtain DNS automatically or to enter DNS manually
#. For **Editing Hosts File**, turn **On** to add or remove hosts in the Hosts file
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control DNS** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
