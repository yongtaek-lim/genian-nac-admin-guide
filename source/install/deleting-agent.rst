Deleting Agent
==============

You can uninstall the Agent on the endpoints by using a Group Policy which allows you to group many devices together and uninstall the Agent as each device comes onto the network. This is useful if you have a large number of devices that will no longer be seen on the network. (*e.g. A School with Seniors graduating will have no need for the Agent to remain on their devices.*)

Create Node Group To Delete Agent
---------------------------------

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the Policy panel
#. Go to **Tasks > Create New Policy Group**

Under **General**

#. For **ID**, type unique name.
#. For **Application Mode**, select **Enable**

Under **Condition**

#. For **Boolean Operator**, select **OR** from drop-down
#. For **Settings**, click **Add**
#. Enter the following condition:

   -  **Options: MAC** from drop-down
   -  **Operator: is equal to** from drop-down
   -  **Value** is the MAC Address of Node (*e.g. XX:XX:XX:XX:XX:XX*)

#. Click **Update**

Delete Agent Using Policy
-------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the Policy panel
#. Go to **Tasks > Create**

Under **Agent** tab

#. Click **Next**

Under **General** tab 

#. For **ID** , type unique name. (*e.g. ID = “Delete Agent”*)
#. Click **Next** 

Under **Node Group** tab 

#. Double click **Delete Agent Group**
#. Click **Next**

Under **Policy Preferences** tab 

#. Click **Next**

Under **Agent Action** tab 

#. Click **Next**

Under **Threat Definition** tab 

#. Click **Finish**

.. attention:: In **Node Policy**, you should see your newly created Policy and a number of **Node(s)** in Nodes column(*Device will not be prompted to do anything upon connecting to the network. Administrator will soon see these Nodes without the Agent Icon in the Management Node list*)

