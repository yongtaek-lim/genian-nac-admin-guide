Deleting Nodes
==============

You can delete inactive Node data to better organize the networks Node view. You can delete inactive Nodes through policies, 
or manually delete Nodes as they are no longer found on the network.

.. note:: The Policy Server keeps Node information by default up to 3 days after an IP has been changed. This time period can be changed by going to **Preferences > General > Node > Lifetime** section.

Remove Inactive Nodes Through Policy
------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Find and click **Policy Name** in the Node Policy window
#. Find **Management Policy > Deleting Node Down** section in the Node Policy window
#. Set a time for deleting Nodes after a period of inactivity (*If a Node is offline for a certain period of time, it will be deleted automatically. Default is 30 days*)
#. Click **Update**

Manually Remove Inactive Nodes
------------------------------

#. Go to **Management > Node** in the top panel
#. Find desired inactive Nodes. Click **Checkbox**
#. Click **Tasks > Node / Device Management > Remove Node** 

.. warning:: If a connected and running node is accidentally deleted, that node will instantly re-register. 

