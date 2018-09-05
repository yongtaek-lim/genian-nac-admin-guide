Configuring Wireless Connection Manager
=======================================

Policy Server communicates with the Agent to configure Wireless Connections with auto-connect, 
auto-reconnect, preferring specific networks, and much more

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Wireless Connection Manager** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **WLAN Policy**, click **Assign** to assign a WLAN Policy
#. For **Wireless Connection Manager**, turn **On** to enforce Wireless Connection Manager

   - **Enforcing Wireless Connection Manager**, turn **On** to enable Wireless Connection Manager
   - **Hiding Wireless Connection Manager for Wired**, specify whether to hide Wireless Connection Manager when a wired network is connected
   - **Auto-Reconnect**, specify whether to automatically reconnect to a wireless network allowed with the strongest signal
   - **Password Expiry Notification**, adjust time to allow a user to change password (*hours - months*)
   - **Preferred Wireless Network**, specify whether the user connects to preferred wireless or wireless with strongest signal
   - **Display Username**, use this field to display Username
   - **Display Password**, use this field to display Password
   - **Enabling Save Username**, turn **On** to allow user to save Username
   - **Enabling Save Password**, turn **On** to allow user to save Password
   - **Enabling Auto-Connect**, turn **On** to allow the latest wireless network to be connected automatically
   - **Window Image**, click **Upload** to load a BMP file for the dialog box
   - **Window Color**, specify a color for the dialog box
   - **Font Color**, specify a color for the text in the dialog box
   - **Contents for Window**, type to enter contents in the dialog box
   - **HTML**, turn **On** to use HTML for contents to be displayed in the dialog box
   - **Program at Log On**, click **Add** to add a Program to launch when user logs in. Specify Path or CLI parameter
   
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Wireless Connection Manager** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
