Update Windows
==============

Genian NAC supports patching of Windows devices using the Agent Action “Update Windows”. 
Policy Server pulls down the latest Windows Updates and Patches periodically to help keep your endpoint devices current. 
With the Agent installed on the endpoints, you can control whether they are getting updates and how often.

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Update Windows** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value** 

Under **Plugin Settings** section

#. For **Windows Update Settings**, select a Windows Update Setting from drop-down, Or click + to create an Update Setting
#. For **Scheduled Check**, specify whether to check for updates on a scheduled basis

   - **Periodic Interval**, adjust the time interval to check for updates (*hours - months*)

#. For **Installation Mode**, specify between Custom or Background Installation
#. For **Operation Mode**, specify whether to check for updates or install the updates
#. For **Scheduled Installation**, specify whether to install the updates on a scheduled basis
#. For **Restart Options**, specify whether to Prompt or Restart
#. For **Automatic Update**, specify whether to check for important updates and install them using settings from drop-down
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Update Windows** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
#. Click **Apply** in top right corner

Create New Windows Updates For Specific OS or Patches
-----------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Node Policy > Agent Action > Windows Update** in the left Policy panel
#. Click **Tasks > Create**

Under **General** and **Automatic Approval Options**

#. For **ID**, type in unique name
#. For **Description**, type in brief description
#. For **Products**, (*Select ones that apply, or All*)
#. For **Classifications**, (*Select ones that apply, or All*)
#. Click **Create**
#. Click **Apply** in top right corner

or

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Update Windows** in the Agent Action window
#. Find **Agent Action: Windows Update Settings** section and click **Edit**

Under **General** and **Automatic Approval Options**

#. For **ID**, type in unique name
#. For **Description**, type in brief description
#. For **Products**, (*Select ones that apply, or All*)
#. For **Classifications**, (*Select ones that apply, or All*)
#. Click **Create**
#. Click **Apply** in top right corner

(*To delete Windows Updates that were created and no longer used go to Policy > Node Policy > Agent Action > Windows Update > click Checkbox of desired update > Tasks > Delete*)

.. toctree::
   :maxdepth: 1

   syncer-software
  
