Creating Wireless Groups
========================

A **Wireless Group** is any detected amount of **SSIDs** that are grouped together due to conditions or properties that have been set to an identifier. This is to help Network Administrators quickly navigate to specific **SSIDs** or **Categories** when dealing with a large quantity of SSIDs.

Create a WLAN Group
-------------------

You can create WLAN Groups to better categorize your SSIDs

#. Go to **Policy** in the top panel
#. Go to **Group > WLAN** in the left Policy panel
#. Click **Tasks > Create**

Under **General**

#. For **ID**, type unique name
#. For **Description**, type what this group consists of
#. For **Application Mode**, select **Enabled** from drop-down
#. For **Generating Logs** (*Optional setting. It is Off by default*)

Under **Condition**

#. For **Boolean Operator** choose **AND** to match all conditions, or **OR** to match any conditions
#. For **Settings** click **Add** to add conditions

Under **Settings**

#. For **Options**, select desired option from drop-down
#. For **Operator**, select desired option from drop-down
#. For **Value**, select desired option from drop-down
#. For **Description**, type what this condition does
#. Click **Add**
#. Click **Save**

Assign a WLAN Tag
-----------------

#. Go to **Management > WLAN** in the top panel
#. Find and click **Checkbox** of desired **SSIDs**
#. Click **Tasks > Assign WLAN Tag**

Under **Assign WLAN Tag**

#. In drop-down select **Assign Selected Tags**
#. Click **Checkbox** of tag to apply
#. Click **Save**
#. Click **Apply**

Assign a WLAN Group
-------------------

#. Go to **Management > WLAN** in the top panel
#. Find and click **Checkbox** of desired **SSIDs**
#. Click **Tasks > Assign WLAN Group**

Under **Assign WLAN Group**

#. For **Action**, select **Add** or **Remove**
#. For **WLAN ID**, select **SSID, MAC,** or **MAC+SSID**
#. For **WLAN Group**, group to associate to
#. Click **Save**
#. Click **Apply**

Group by Network Sensor
-----------------------

#. Go to **Management > WLAN** in the top panel
#. Click **Edit Tree icon** in the top right corner
#. Right click on either **WLAN AP** or **WLAN Client** to assign a Sensor

   - In case you have many **Sensors**, you can create a subfolder by selecting **Create** option

#. Search for a **Network Sensor** and select one
#. Click **OK**
