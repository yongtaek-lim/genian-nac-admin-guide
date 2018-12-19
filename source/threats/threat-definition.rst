Creating Anomaly Definition
===========================
 
The Anomaly you defined is here used when detecting an Anomaly with a Node Policy.
This is a definition setting, therefore, you must assign the configured definition to the Node Policy you would like to apply. 

By default, there are eight pre-defined **Anomaly Definitions** that are frequently used. With the steps provided below, you can create your own Anomaly Definitions.

To Create an Anomaly Definition
-------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Tasks > Create**

Under **General**

#. For **ID**, type unique name
#. For **CWP Message**, enter message to be presented to user
#. For **User-defined Severity**, choose **Low, Medium,** or **High** for Anomaly severity
#. For **Status**, must be **Enabled** to be active
#. For **Node Group Exception**, optional setting to choose group to be an exception to this Anomaly

Under **Anomaly Event**

#. For **Event**, choose which Anomaly Definition to use
#. For **Options**, customize the options as needed based on selected **Event**
#. Click **Create**

To Delete an Anomaly Definition
-------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Anomaly Definition** in the left Policy panel
#. Click **Checkbox** of desired **Anomaly Definition**
#. Click **Tasks > Delete**
#. Click **OK**
#. Click **Apply**