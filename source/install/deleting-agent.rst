Deleting Agent
==============

You can uninstall the Agent on the endpoints either by using a Node Policy which allows you to
group many devices together or by using an Authentication Code which allows you to delete an individual agent.  

Delete Agent Using Policy
-------------------------

This method is ideal for deleting the agent from a large number of devices, without end user involvement.

#. Create a **Node Group** to select which nodes to delete agent.

#. Create a **Node Policy** to delete agent from the selected nodes.
  
   - Under: **Policy Preferences** find the  **Agent Policy** section and set the **Agent** drop down menu to **Delete**.

#. After creating the node policy, click the **apply** option in the top right corner. 

This will automate the deletion of the agent from the designated devices when the node policy updates on the agent.  

Delete Agent Using Authentication Code
--------------------------------------

This option is ideal for a user to request agent removal. An administrator can approve this request. 

Deleting as **Endpoint user**:

#. Go to the task bar on Windows or OSX machine and find the Genians logo.
#. Right click the logo and select the ***Delete Agent(D)** option.
#. find the **Agent Code** in the pop up window, and provide it to your Genians NAC Administrator who will use it to generate an **Authentication Code**. 
#. Enter the **Authentication Code** provided into the designated form, and click the **Delete** button.

Claiming ***Authentication Code** as an **Administrator**

#. Log in to Policy server Management console. 
#. Mouse over the **Management** tab on the menu bar and select the **Request** option underneath.
#. In the tree panel on the left of the page, find **Agent Authentication Code**, and select **Generator**
#. Enter the **Agent Code** supplied by the endpoint user and click **Generate** button.
#. An  **Authentication Code** will be displayed. Provide this code to the end user. 

.. note:: Authentication Code based deletion method is still possible when endpoint is offline, as long as policy server is active. 

Delete Agent When Policy Server Is No Longer Available
------------------------------------------------------

The Policy Server used to install the agent is needed to delete the agent. 
If this Policy Server is no longer available, a new policy server is needed.

#. Install new Policy Server.
#. Reinstall Agent from Policy Server using standard agent installation. This will overwrite the existing agent.
#. Delete the agent using Node Policy or Authentication Code. 