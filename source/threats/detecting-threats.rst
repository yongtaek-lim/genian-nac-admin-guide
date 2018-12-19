Detecting Anomalies
===================
 
Once the configured **Anomaly Definition** is assigned to the **Node Policy** you would like to apply, an anomaly will be almost immediately detected either by a **Network Sensor** or by an **Agent**. 
You may see the results in a variety of ways. 

   - Find **Anomaly** column in **Node Management**
   - Edit Node View for **Anomaly View**
   - Trace **Anomaly Logs**
   - Glance **Dashabord Widget** for **Anomaly** tab
   - Filter **Status & Filters**
      
Furthermore, you can be notified about any pre-defined anomalies that are detected. 

For notifying a user about the anomalies detected, please see :doc:`/logs/notification-event` 

Identify Nodes through Policy and Detect them through New Node Policy
---------------------------------------------------------------------

You may create a new Node Policy to exclusively detect an anomaly pre-configured through Anomaly Definition.

.. note:: Steps below are optional to create a new Node Policy if you prefer not to use an existing one

Step 1. Create Policy Group for New Node Policy
-----------------------------------------------

This will group together all Nodes that will be identified by the Node Policy using pre-configured Anomaly Definitions

#. Go to **Policy** in the top panel
#. Go to **Policy > Group > Node** in the left Policy panel
#. Click on **Tasks > Create New Policy Group**
#. For **ID:** Unique Name (*e.g. Anomaly Policy Group*)
#. For **Status:** Enabled 
#. For **Boolean Operator**  select **OR**
#. Find and click on **Add** in **Condition** section
#. For **Condition** you want to add, use the followings:

   - **Options:** (*One of the listed Options*)
   - **Operator:** (*One of the listed Operators*)
   - **Value:** (*One of the listed Values*)

#. Click **Add**
#. Keep adding **Conditions** as needed   
#. Click **Save**

Step 2. Create Node Policy To Detect Anomalies
----------------------------------------------

This will detect all Anomalies identified within the Node Policy and are listed in the Policy Group from Step 1.

#. Go to **Policy** in the top panel
#. Go to **Node Policy** in the left Policy panel
#. Click on **Tasks > Create**
#. **Action** tab, click **Next**
#. **General** tab

   - **ID:** Unique Name (*e.g. Anomaly Detection Policy*)
   - **Description:** Anomaly Policy to detect all Anomalies
   - **Status:** Enabled
   - Click **Next**

#. **Node Group** tab, find and double click **Policy Group** (*e.g. Anomaly Policy Group*). Click **Next**
#. **Policy Preferences** tab, configure any settings as needed. Click **Next**
#. **Agent Action** tab, click **Next**   
#. **Anomaly** tab, select **Anomaly** from **Available** column, and move to **Selected** column for the desired Anomaly to be detected. Click **Finish**  
#. Click **Apply**


Assign Pre-Configured Anomaly Definitions to Node Policy
--------------------------------------------------------

By default the Default Policy is collecting information and is not detecting any anomalies. This will add Anomaly Definitions to the Default Policy and actively detect anomalies.

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click on **name of Node Policy** in the main Node Policy window
#. Find **Anomaly** section. Click **Assign**
#. Select **Anomaly** from **Available** column, and move to **Selected** column
#. Click **Add** 
#. Click **Update**


See Anomaly Detected Through **Anomaly Column** in Node Management
------------------------------------------------------------------

#. Go to **Management > Node** in top panel
#. Find **Anomaly** column and see an icon (*You might be able to see its details by clicking on the icon displayed*)

See Anomaly Detected Through **Anomaly View** in Views
------------------------------------------------------

#. Go to **Management > Node** in top panel
#. Find **Menu (3 dots and lines)** button that places next to Tasks button and click on that
#. Find **Views** and select **Anomaly View**
#. **Threat Detected** and **Threat Definition** columns will appear (*A column may be configurable by clicking* **Edit Columns**)

See Anomaly Detected Through **Anomaly Logs** in Log
----------------------------------------------------
#. Go to **Log > Log** in the top panel
#. Go to **Logs > Anomaly Logs** in the left Log panel

See Anomaly Detected Through **Anomaly Tab** in Dashboard Widget
----------------------------------------------------------------
#. Go to **Dashboard** in the top panel
#. Go to **Anomaly** tab

See Anomaly Detected Through **Anomaly Definition and Anomaly Detection** in Status & Filters
---------------------------------------------------------------------------------------------
#. Go to **Management > Node** in the top panel
#. Go to **Status & Filters > Anomaly Detection and Node with Anomaly** in the bottom left panel

Clear Anomaly Detection Records
-------------------------------

#. Go to **Management > Node** in top panel
#. Find and click **Checkbox** of desired Nodes
#. Click **Tasks > Node / Device Management > Clear Anomaly Records**
#. Click **OK**