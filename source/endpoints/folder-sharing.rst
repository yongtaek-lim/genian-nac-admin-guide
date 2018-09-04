Controlling Network Folder Sharing
==================================

You can collect shared network folder information, control access, and specify permissions

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Network Folder Sharing** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Collecting Shared Folder Information**, select **Off** to not collect info about shared folders over the network
#. For ** Stopping Folder sharing**, turn **On** to stop folder sharing

   - **Delay Timeout**, specify the time when the shared folder access is revoked (*seconds - months*)
   - **Read-only Folder Exception**, turn **On** to allow access to the folder with read-only permissions
   - **Stopping Everyone Folder Only**, turn **On** to stop sharing the folder with everyone permissions
   - **Administrative Shares Exception**, select **Off** to disable access to the Administrative Share

#. For **Folder Sharing Expiry Notification**, select Custom Message or Default Message in Pop-up window
#. Click **Update**
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find Agent Action. Click Assign
#. Find **Control Network Folder Sharing** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
