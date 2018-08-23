Controlling Screen Lock
=======================

You can control the screen lock on your Windows devices which requires users to authenticate upon wake from sleep. 
You can also force to use specific wallpaper image (*e.g. Library Nodes, or Store Front Nodes*)

See the Configuration of the Plugin
-----------------------------------

- Go to **System > Update > Genian Software > Plugin > Control Screen Lock**

Add the Agent Action to a Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Screen Lock** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Control Screen Lock
-------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Screen Lock** in the Agent Action window
#. Enter in **Conditions**, and adjust **Agent Actions** based off of your network requirements
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
