Node Group based Access Control
===============================

While **Node Policies** are mainly used for collecting information from Nodes, **Enforcement Policies** are typically called blocking policies which block the endpoint from accessing the network and redirecting to a **Captive Web Portal** for instructions on being compliant. Once **Node Groups** are created,(:doc:`/monitoring/network-nodes/creating-nodegroups`) controls can be defined by creating **Enforcement Policies**. These policies can then be applied to the **Node Group** to enforce those conditions upon the Nodes within the Group.

.. toctree::
   :maxdepth: 1

   nodegroup-control/permissions
   nodegroup-control/policy-nodegroup
   nodegroup-control/managing-status
   nodegroup-control/enforcement-agentaction
   