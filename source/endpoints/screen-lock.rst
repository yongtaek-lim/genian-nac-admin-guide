Controlling Screen Lock
=======================

You can control the screen lock on your Windows devices which requires users to authenticate upon wake from sleep. 
You can also force to use specific wallpaper image (*e.g. Library Nodes, or Store Front Nodes*)

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Screen Lock** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Lock Screen Scan**, select **Off** to disable the collection of info on the configured Screen Lock
#. For **Reauthentication**, turn **On** to require User Authentication from Wake or Screen Lock
#. For **File Integrity Check Interval**, adjust time interval to check Screen Lock integrity (*minutes - hours*)
#. For **Lock Screen Enforcement**, turn **On** enforce a Screen Lock

   - **Waiting Time**, specify the time before the Screen Lock starts (*minutes - hours*)
   - **User Waiting Time**, this will not apply if this time is longer than Waiting Time
   - **Displaying Logon Screen**, displays logon screen upon Resume
   - **Genian Lock Screen Message**, type message to display on Screen Lock
   - **File**, upload a file to be used for Screen Lock 
   - **File Name**, define a name for the Screen Lock File
   - **User-configured Lock Screen**, select **Off** to not allow a User to configure Screen Lock

#. For **Wallpaper Image Enforcement**, turn **On** to enforce a Desktop Wallpaper

   - **File**, upload a file to be used for Wallpaper
   - **File Name**, define a name for the Wallpaper File
   - **Position**, specify the position of the Wallpaper File (*Center, Tile, Stretch*)  

#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Screen Lock** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Add Authentication Code to Unlock Screen Lock
---------------------------------------------

You can enable a Authentication Code for when users are unable to authenticate and unlock their screens from Screen Lock.
Users can sometimes be offline and will need to authenticate to unlock their screens. 
The option below provides a button to generate a Agent Code to give to the Administrator to then get a Authentication Code 
to enter into the Screen Lock.

.. note:: **Control Screen Lock** must already be configured and enabled in the Node Policy (*Default Policy*)

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Authenticate User Using Genian Agent** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
#. Go to **Policy > Node Policy > Agent Action**, click on **Authenticate User Using Genian Agent**

Under **Agent Action: Miscellaneous**

#. For **Authentication Enforcement**, turn **On** Screen Lock Authentication
#. For **Page Background Color**, optional setting to change the background color
#. For **Displaying Unlock Screen**, turn **On** to display a **Unlock Screen Button**
#. Click **Update**

.. note:: User clicks "Unlock Screen Button" to generate "Agent Code" and gives to Administrator. Administrator then uses this to get "Authentication Code" for user to enter in and "Unlock Screen Lock"
