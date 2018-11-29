Creating Node Groups
====================

A **Node Group** is a group of **Nodes** that are similar to each other based off of certain conditions. **Node Groups** allow you take action on many **Nodes** at once versus the same action on many individual **Nodes**. Genian NAC provides two types of **Node Groups** that can be applied to **Node Policies** and **Enforcement Policies**

- **Policy Group**: is group based on Node-related information such as Node type, IP/MAC information, User information, Authentication, and more. `Policy Group`_
- **Status Group**: is group based on the Node status, measured by Node Policies and the outcome of associated conditions. `Status Group`_

#. Click **Policy** in the top panel
#. Go to **Group > Node** in the left Policy panel
#. Click **Tasks > Create New Policy Group** or **Create New Status Group**

Under **General**

#. For **Category**, Choose default or Create New (*This allows you to categorize your Node Groups*)
#. For **ID**, type unique name
#. For **Description** (*Brief description of what this Node Group is for*)
#. For **Application Mode**, **Enabled**

#. Enter the following in Condition section:

   - Boolean: “**AND**” or “**OR**” (*”AND” all conditions have to apply. “OR” any of the conditions have to apply*)
   - Settings: Click **Add** (*These are the various conditions to be applied for proper grouping*)

#. Click **Add**
#. Click **Save**
#. Click **Apply** in top right corner

.. _Policy Group: https://www.genians.com/concepts/#node-groups
.. _Status Group: https://www.genians.com/concepts/#node-groups
