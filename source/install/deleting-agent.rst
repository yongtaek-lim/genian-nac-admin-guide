Deleting Agent
==============

You can uninstall the Agent on the endpoints by using a Group Policy which allows you to group many devices together and uninstall the Agent as each device comes onto the network. This is useful if you have a large number of devices that will no longer be seen on the network. (*e.g. A School with Seniors graduating will have no need for the Agent to remain on their devices.*)

To Create Node Group To Delete Agent
------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the Policy panel
#. Go to **Tasks > Create New Policy Group**
#. Find **General: ID** and enter Delete Agent Group for a unique name
#. Find **General: Application Mode** and verify it is set to Enable
#. Find **Condition: Boolean Operator** section and select OR from drop-down
#. Find and click on the **Add** button in **Condition: Settings** section
#. Enter the following condition:

   -  **Options: MAC** from drop-down
   -  **Operator: is equal to** from drop-down
   -  **Value** is the MAC Address of Node (*e.g. XX:XX:XX:XX:XX:XX*) 
   
   `(*You can have many Nodes*)`

#. Click **Update**

To Delete Agent Using Policy
----------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the Policy panel
#. Go to **Tasks > Create**
#. **Agent** tab click **Next**
#. **General** tab enter name for **ID** and click **Next** (*e.g. ID = “Delete Agent”*)
#. **Node Group** tab double click **Delete Agent Group** and click **Next**
#. **Policy Preferences** tab click **Next**
#. **Agent Action** tab click **Next**
#. **Threat Definition** tab click **Finish**

#. In **Node Policy**, you should see your newly created Policy and a number of **Node(s)** in Nodes column 
(*Device will not be prompted to do anything upon connecting to the network. Administrator will soon see these 
Nodes without the Agent Icon in the Management Node list*)