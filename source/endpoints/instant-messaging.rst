Collecting Instant Messaging Application Information
====================================================

Policy Server communicates with the Agent to collect instant messaging application information on 
end users Windows devices. (e.g. Aim, GoogleTalk, Yahoo, MSN and more)

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Collect Instant Messaging Application Information** in the Agent Action window

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
#. Find **Collect Instant Messaging Application Information** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
