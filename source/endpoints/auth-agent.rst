Authenticate User Using Genian Agent
====================================

Policy Server communicates with the Agent to collect TCP Connection Information periodically and disables a network interface that exceeds the configured connection limits.

Add the Agent Action to a Policy
--------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Authenticate User Using Genian Agent** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

Authenticate User Using Genian Agent
------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Authenticate User Using Genian Agent** in the Agent Action window
#. Enter in **Conditions**, optional settings

Under **Authentication Policy**

#. For **Authentication Methods**, Select a method to authenticate a user
#. For **2-Step Authentication**, Select a 2-Step Authentication method

Under **Agent Authentication Dialog Box Design**

#. For **Window Image**, Specify an image for the Agent authentication dialog box
#. For **Displaying Titlebar**, Specify whether to display a titlebar on the Agent authentication dialog box
#. For **Dialog Box Color**, Specify a dialog box color
#. For **Font Color**, Specify a font color
#. For **HTML Help Message**, Specify a HTML Help Message

Under **Miscellaneous**

#. For **Authentication Enforcement**, Specify whether to enforce an authentication by disabling the close action for the Agent Authentication dialog box
#. For **Program Run after Authentication**, Add a program that is run after a user is successfully authenticated
#. Click **Update**
