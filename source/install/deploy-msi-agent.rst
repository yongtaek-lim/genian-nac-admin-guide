To configure GPO in Active Directory
====================================

Describes how to set up a GPO that can deploy the Genian Agent MSI in AD.

Step 1. Create a shared folder for the deploying MSI files
----------------------------------------------------------

- Copy the Agent MSI file from Genians to a shared folder or set the folder that contains the file as a shared folder

Step 2. Open the **Group Policy Management** and to make the GPO
----------------------------------------------------------------

- **Run** > **gpmc.msc** or **Start** > **Administrative Tools** > **Group Policy Management** in Window server
- Expand the **[domain name]** on the left panel > Click the **Group Policy Object** on the mouse right button > Click the **New** > Put the **Name(ex. genian)** > **OK**
- Click the **genian** GPO on right mouse button > **Edit** You can see the **Group Policy Management Editor**

Step 3. To configure the **Group Policy Management Editor**
-----------------------------------------------------------

- Expand the **Policies** and **Software Settings** folder in left panel > click the **Software installation** > Click the right mouse button in right panel and click the **New** and **Package**
- To move on share folder path like (ex. \\[domain]\Share folder) and then select the Agent MSI file > select **Advanced** in **Deploy Software popup** 
- Click the **Deployment** tab > check the **Uninstall this application when it falls out of the scope of management** > click the **advanced** > check the **Ignore language when deploying this package** > **OK**

Step 4.To apply the GPO policy in **Group Policy Management**
-------------------------------------------------------------

- Click the **Computers** folder on the mouse right button in left panel > click the **Link an Existing GPO** > Select the **genian GPO**

Step 5. Verification
--------------------

GPOs can contain both **computer** and **user** sets of policies. 
The **Computer section** of a GPO is applied during boot. 
The **User section** of a GPO is applied at user login.

- **run** > **cmd** > put the command **gpupdate /force**
- Check the **GnAgent.exe, GnPlugin.exe, GnStart.exe** process in the **task manage**
- Check for Agent files existent like **GnAgent.exe, GnPlugin.exe, GnStart.exe** in C:\Program Files\Geni\Genian





