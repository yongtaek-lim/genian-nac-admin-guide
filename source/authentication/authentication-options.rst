Configuring User Authentication Options
=======================================

Authentication Criteria
-----------------------
 
Set the authentication criteria for user authentication. When a user is identified through CWP or SSO, 
you can choose whether to reflect that user information on the node (IP + MAC) or on all devices to which the node belongs. 

For example, in a laptop with two network interfaces, if user authentication is performed through one of the nodes, 
only the node that has been authenticated should set user information or all nodes of the device that has been authenticated 
should set user information You can choose.

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > User Authentication** in the left Preferences panel
#. For **Authentication Criteria**, select **Node** if you want users to Authenticate to the Node or select **Device** if you want users to Authenticate to the Device
#. Click **Update**

Automatic Device Ownership
--------------------------

Device owner information can be managed separately from user information. In many cases, the owner and the user of the device are the same,
so if the device does not have owner information, the ability to automatically update authenticated user information with owner information is provided.

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > User Authentication** in the left Preferences panel
#. For **Automatic Ownership**, select **On** to automatically assign ownership
#. For  **Criteria**, specify a scope to assign User and Department. **IP**, **MAC**, **IP + MAC**
#. For  **Update options**, select between **When it is not assigned** or **When a User is authenticated** to reassign User and Department
#. Click **Update**

Find Username & Password
------------------------

To setup the ability for your users to find out what their username or password is with a security question

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > User Authentication** in the left Preferences panel
#. For **Find Username / Reset Password**, select **On**
#. For **Find Username**, select finding method
#. For **Reset Username**, select finding method
#. Click **Update**

Authentication Lifetime
-----------------------

The Authentication Lifetime is the length of time, in minutes, before the authentication expires and the user must log in again. 
You can configure Authentication Lifetimes for Users, and Nodes

Configure User Authentication Lifetime
''''''''''''''''''''''''''''''''''''''

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click desired Node Policy for change configuration
#. Find **Advanced > Authentication Policy > Automatic Log Out**. Select **On**
#. Specify how long **User** stays logged on
#. Click **Update**

Configure Node Authentication Lifetime
''''''''''''''''''''''''''''''''''''''

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click desired Node Policy for change configuration
#. Find **Advanced > Authentication Policy > Automatic Log Out for Node**. Select **On**
#. Specify how long **Node** stays logged on
#. Click **Update**

Login restriction
-----------------

You can restrict users or groups that can log in by node policy or individual nodes.

Restriction by node policy
''''''''''''''''''''''''''

For all nodes with a specific node policy, you can specify a group of users who can log in when authenticating the user.

#. Go To **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click desired Node Policy for change configuration
#. Find **Advanced > Authentication Policy > Auth User Group**. Select the user group you want to allow to login
#. Click **Update**

Restriction by individual node
''''''''''''''''''''''''''''''

#. Go To **Managent > Node** in the top panel
#. Find the node for which you want to set the policy
#. Click **IP Address** and select Policy tab
#. Under **Authentication Policy**, select **Require Authentication (Allow specific user(s))**
#. Assign user or user group using **Assign** button
#. Click **Update** button on bottom