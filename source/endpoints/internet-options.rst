Control Internet Explorer Security Settings
===========================================

You can control the Security Settings of Internet Explorer on end users Windows devices. 
You can configure the options under General, Security, Content, and Connections tabs,  as well as Add-Ons. 
Additionally, you can change browser settings using Add-on Controls

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Internet Explorer Security Settings** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Internet Options General**

   - **Home Page**, specify a home page or leave blank to not control
   - **Empty Temporary Internet Files Folder**, select **Enforce** to delete all the temporary internet files stored during the session

#. For **Internet Options Security**

   - **Downloading Unsigned ActiveX Controls**, select **Disable** to not download unsigned ActiveX controls
   - **Automatic Prompting for ActiveX Controls**, select **Disable** to disable the automatic prompting notifications
   - **Automatic Prompting for File Downloads**, select **Disable** to disable the automatic prompting for download attempts
   - **Blocking Pop-up**, select **Enforce** to prevent most pop-up windows from appearing
   - **Trusted Sites**, turn **On** to add or remove Trusted Sites. Also can **Enable** and **Disable Server Vierifications**

#. For **Internet Options Connections**

   - **Proxy Server**, specify whether to use or how to use a proxy server for User LAN (*These settings will not apply to dial-up or VPN*)
   
      - **Do Not Use**, does not utilize the **Proxy Server**
      - **Use Proxy Server**, add Address Port, enable optional Bypassing Proxy Server, enter in exceptions
      - **Configure Advanced Settings**, enter HTTP, Secure, FTP, Socks Ports. Enable optional Bypassing Proxy Server, enter in exceptions

#. For **Internet Options Content**

   - **AutoComplete for Forms**, select **Disable** to prevent auto completion of forms

#. For **Add-on Controls**

   - **Deleting Unused ActiveX Control**, turn **On** to delete unused ActiveX Controls installed
   - **Removing Toolbar**, turn **On** to remove Toolbar 
   - **Removing Browser Helper Object**, turn **On** to remove Browser Helper Object 
   - **Exceptions**, type name of Add-ons to not be removed

#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Internet Explorer Security Settings** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

