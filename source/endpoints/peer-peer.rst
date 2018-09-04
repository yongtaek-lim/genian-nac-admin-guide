Collecting Peer-to-peer Application Information
===============================================

Policy Server communicates with the Agent to collect peer-to-peer application information on 
end users Windows devices. (*e.g. Torrent, Ares, BearShare, Shareaza, and more*)

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect Peer-to-peer Application Information** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Action** section

#. For **Boolean Operator**, leave as default **AND**
#. For **Settings**, leave the default and click **Add** button to include others if they are not listed
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Collect Peer-to-peer Application Informatio**n in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
