Configuring GenianSyncer Software
=================================

GenianSyncer Software is designed to get Microsoft Updates and Patches from Microsoft website and sync with a Policy Server that cannot access the internet. GenianSyncer Software gets installed on a Windows machine to be able to download Microsoft Updates and Patches from the Microsoft website and be used as an internal repository. You can then set up the Policy Server to periodically sync with the Windows Machine to proxy to endpoint devices using the “Update Windows” Agent Action.

To Download and Install GenianSyncer Software
---------------------------------------------

#. Contact **Genians** to get **GenianSyncer Software**
#. **Download GenianSyncer.zip**
#. **Unzip GenianSyncer.zip**
#. **Run GenianSyncer.exe** (*New dialog window will appear*)
#. Click **Get Started** in new GenianSyncer dialog window (*New dialog window will appear*)
#. Enter **Policy Server Address**
#. Update **Options** (*You can specify Classifications and Products to narrow down the scope of the files you will download*)
#. **Specify a folder to Download to** by clicking the **three dotted icon**
#. Click **Register License** to activate a GenianSyncer

   - **Download** (*e.g. C:#Program Files [x86]#Geni#GenianSyncer*)
   - Click **Upload License** File
   - **License**
   - **Genian Data URL** (*e.g. https://geniupdate.geninetworks.com/geniupdate/v###.php*)

      - **How To Find Genian URL?**
      - Login to **Policy Server CLI**
      - **cat /disk/data/system/logs/centerd | grep geniupdate.geninetworks.com** (*e.g. https://geniupdate.geninetworks.com/geniupdate/v450.php*)
      - Copy this **URL** into **Genian Data URL**
      - Exit **Policy Server CLI**

   - **Speed** option (*You can limit the upload or download speed by specifying the Maximum speed*)
   - Click **OK** (*New dialog window will appear*)

#. Click **Download From Policy Server** to access the Policy Server
#. Enter a **Policy Server IP Address** or **Hostname**. Then enter **Username** and **Password** and click **OK**
#. Click on **Download From Internet** to download the files from Microsoft (*This must be done upon the first time of setting this up*)
#. Click **Upload To Policy Server** to upload the updates and patch files to the Policy Server
#. Enter a **Policy Server IP Address** or **Hostname**. Then enter **Username** and **Password** and click **OK**
#. **No uploaded files found** (*If “No uploaded files found. Would you like to upload the GENIAN DATA?”) Click **OK**
#. Click **OK** when files have been uploaded to the Policy Server successfully

To Verify Updates and Patches Uploaded Successfully
---------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Node Policy > Agent Action > Windows Update** in the left Policy panel
#. Click the **desired Update name** in Windows Update Settings window
#. Find and click **Update** tab (*You will see the new Updates and Patches*)

To Configure Update Service Settings
------------------------------------

(*This is instructing the Agent to look for the Updates and Patches from the Policy Server versus the internet*)

#. Go to **Preferences** in the top panel
#. Go to **General > Agent > Update Service** in the left Preferences panel
#. Find **Windows Update: Check for Updates** section. Select **Local Repository**
#. Click **Update**

To Configure Appliance Settings
-------------------------------

(*This is instructing the Policy Server to Proxy Updates and Patches to Agents*)

#. Go to **System** in the top panel
#. Go to **System, click Policy Server IP Address > Appliance** tab
#. Find **Proxy for Windows Updates** section. Select **On to Proxy Services**
#. Click **Update**
