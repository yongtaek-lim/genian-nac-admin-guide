Controlling Network Access Based On Node Group
==============================================

While **Node Policies** are mainly used for collecting information from Nodes, **Enforcement Policies** are typically called blocking policies which block the endpoint from accessing the network and redirecting to a **Captive Web Portal** for instructions on being compliant. Once **Node Groups** are created,(`Creating Node Groups`_) controls can be defined by creating **Enforcement Policies**. These policies can then be applied to the **Node Group** to enforce those conditions upon the Nodes within the Group.

.. toctree::
   :maxdepth: 2

   policy-nodegroup
   managing-status
   enforcement-agentaction

.. _Creating Node Groups: https://www.genians.com/docs/administrators-guide/?section=creating-node-groups