Applying policies using tagging
===============================

The purpose of this function is to assign a tag to a target where a specific log is generated, 
and then to apply the policy by creating a group based on the tag.

How to use the tag feature
--------------------------

#. Create the Tag
#. Assign Tag after searching target to assign Tag using Log Filter
#. Create "Node Group" for tag assignment
#. Applying policies using "Node group"

Create the Tag
--------------

Refer to the way how to `create the Tag`_ 

Assign Tag after searching target to assign Tag using Log Filter
----------------------------------------------------------------

#. Go to **Log** in the top panel
#. Go to **Search** in the left Log panel
#. Search for logs to assign tags using **Filter** (Filter: IP, MAC, Username, Full Name, Description)

ex) Search for targets with anomaly records and then Put the "Anomaly" in **Description**

4. Click the **Search** button and check the Log list that contains the information you want.
5. Click the **Save As** button
6. To make the **Log filter**, Put the *Name*
7. Click the **check-list** beside **Tag** and select the **Assign**

- **From**: The [Node/External device/User/WLAN] that generated the log
- **To**: The [Node/External device/User/WLAN] to which the tag is assigned
- **Tag**: Tag to assign

.. note:: If you want to delete a Tag, Select the **clear**

8. Verification

- Click on the IP after searching for the target to which the tag is assigned
- Check the Tag assigned to the target in the **General Tab**.

Create "Node Group" for tag assignment
--------------------------------------

Conditions for Node Groups

- Options: Tag
- Operator: is equal to
- Value: [Tag name]

Refer to `Creating Node Groups`_


Applying policies using "Node Group"
------------------------------------

Refer to `Creating Enforcement Policy for Node Group`_

.. _Create the Tag: https://docs.genians.com/monitoring/network-nodes/tagging-nodes.html?highlight=properties#create-tag
.. _Creating Node Groups: https://docs.genians.com/monitoring/network-nodes/creating-nodegroups.html?highlight=create%20new%20policy#creating-node-groups
.. _Creating Enforcement Policy for Node Group: https://docs.genians.com/controlling/enforcement-policy/policy-nodegroup.html#creating-enforcement-policy-for-node-group
