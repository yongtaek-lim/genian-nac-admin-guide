Deleting Agent
==============

You can uninstall the Agent on the endpoints either by using a Node Policy which allows you to
group many devices together or by using an Authentication Code which allows you to delete an individual agent.  

Delete Agent Using Policy
-------------------------

Create a node group to select nodes to delete agent from. This is useful if you have a large number
of devices that will no longer be seen on the network. For example: A School with Seniors graduating 
will have no need for the Agent to remain on their devices.

#. Go to **Policy** in the top panel
#. Go to **Group > Node** in the Policy panel
#. Go to **Tasks > Create New Policy Group**

Under **General**

#. For **ID**, type unique name:**[Delete Agent Group]**.
#. For **Status**, select **Enabled**

Under **Condition**

#. For **Boolean Operator**, select **OR** from drop-down
#. For **Settings**, click **Add**
#. Enter the following condition:

   -  Select: **Options: , Operator:** and **Value** to choose which criteria to select nodes by.

#. Click **Update**

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the Policy panel
#. Go to **Tasks > Create**

Under **Action** tab

#. Click **Next**

Under **General** tab 

#. For **ID** , type unique name. (*e.g. ID = “Delete Agent”*)
#. Click **Next** 

Under **Node Group** tab 

#. Drag  **Delete Agent Group** to selected collumn.
#. Click **Next**

Under **Policy Preferences** tab 

#. Scroll down to **Agent Policy** section.
#. Select **Delete** from the drop down menu to the right of "Agent".

Under **Agent Action** tab 

#. Click **Next**

Under **Anomaly Definition** tab 

#. Click **Finish**

.. attention:: In **Node Policy**, you should see your newly created Policy and a number of **Node(s)** in Nodes column(*Device will not be prompted to do anything upon connecting to the network. Administrator will soon see these Nodes without the Agent Icon in the Management Node list*)

Delete Agent Using Agent Code
-----------------------------
This option is ideal for when a single device is scheduled to be decommissioned from the environment, but will be used by another organization or individual who does not require te agent.

Deleting as **Endpoint user**:

#. Go to the task bar on Windows or OSX machine and find the Genians logo.
#. Right click the logo and select the ***Delete Agent(D)** option.
#. find the **Agent Code** in the pop up window, and provide it to your Genians NAC Administrator who will use it to generate an **Authentication Code**. 
#. Enter the **Authentication Code** provided into the designated form, and clicke the **Delete** button.

Claiming ***Authentication Code** as an **Administrator**

#. Log in to Policy server Management console. 
#. Mouse over the **Management** tab on the menu bar and select the **Request** option underneath.
#. In the tree panel on the left of the page, find **Agent Authentication Code**, and select **Generator**
#. Enter the **Agent Code** supplied by the endpoint user and click **Generate** button.
#. An  **Authentication Code** will be displayed. Provide this code to the end user. 

.. note:: Agent Code based deletion method is still possible when endpoint is offline, as long as policy server is active. 

Delete Agent When Policy Server Is No Longer Available
------------------------------------------------------

The Policy Server used to install the agent is needed to delete the agent. 
If this Policy Server is no longer available, a new policy server is needed.

#. Install new Policy Server.
#. Reinstall Agent from Policy Server using standard agent installation. This will overwrite the existing agent.
#. Delete the agent using Node Policy or Authentication Code. 