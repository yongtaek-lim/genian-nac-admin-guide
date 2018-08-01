Single Sign-On via AD Domain Login
==================================

Genian NAC Windows agent can read Active Directory domain logon user information and use it to authenticated user information for nodes.

#. Go to **Policy** in top panel
#. Go to **Node Policy** in the left Policy panel
#. Find and click **Default Policy** to use this policy (*You can create a custom policy*) :doc:`/controlling/policy-nodegroup`
#. Find **Authentication Policy** section. Select **Active Directory** from drop-down for Federated Authentication
#. Enter **AD Domain Name** when Domain Name (AD) option becomes available
#. Click **Update**
#. Endpoint devices should be logged into the **Domain**