Controlling Windows Update
==========================

Genian NAC supports patching of Windows devices using the Agent Action “Update Windows”. Policy Server pulls down the latest Windows Updates and Patches periodically to help keep your endpoint devices current. With the Agent installed on the endpoints, you can control whether they are getting updates and how often.

To see the configuration of the plugin
--------------------------------------

- Go to **System > Update > Genian Software > Plugin > Update Windows**

To Add the Agent Action to a Policy
-----------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Update Windows** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
#. Click **Apply** in top right corner

To Control Windows Updates
--------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Update Windows** in the Agent Action window
#. Find **General** section (*Name and Description is pre-defined, and CWP Message and Label is optional*)

   - **CWP Message** (*Optional message when user is redirected to CWP*)
   - **Label** (*Optional setting*)

#. Find **Condition** section and add in optional conditions that apply. Click **Add** (*If Boolean Operator is set to “AND“, all conditions have to be met. If set to “OR” any of the conditions can apply*)

#. Find **Agent Action** section and change settings to meet your requirements (*Windows Update Settings drop-down has two by default, All Windows Updates or Default Windows Updates. You can add custom Updates by clicking the Plus Symbol or going to Policy > Node Policy > Agent Action > Windows Update > Tasks > Create*)

   - **All Windows Updates** contains all the Updates and Patches selected for you to use. (*You can customize this but it is suggested to create a New Custom update*)
   - **Default Windows Updates** contains all the settings but nothing selected. (*This is in place for you to quickly select your custom options and save them*)

#. Click **Update**
#. Click **Apply** in top right corner

To Create New Windows Updates For Specific OS or Patches
--------------------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Node Policy > Agent Action > Windows Update** in the left Policy panel
#. Click **Tasks > Create**
#. Enter the Following:

   - **ID**
   - **Description**
   - **Products** (*Select ones that apply or All*)
   - **Classifications** (*Select ones that apply or All*)

#. Click **Create**
#. Click **Apply** in top right corner

or

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Update Windows** in the Agent Action window
#. Find **Agent Action: Windows Update Settings** section and click **Edit**
#. Enter the Following:

   - **ID**
   - **Description**
   - **Products** (*Select ones that apply or All*)
   - **Classifications** (*Select ones that apply or All*)

#. Click **Create**
#. Click **Apply** in top right corner

(*To delete Windows Updates that were created and no longer used go to Policy > Node Policy > Agent Action > Windows Update > click Checkbox of desired update > Tasks > Delete*)

.. toctree::
   :maxdepth: 2

   syncer-software
   
