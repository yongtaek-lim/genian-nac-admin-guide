Single Sign-On via AD Domain Login
==================================

You can configure the **Policy Server** to integrate with Active Directory Domain Login for User Authentication

Enable Node Policy for Gather Active Domain User information
------------------------------------------------------------

#. A **Domain** must be configured in Active Directory
#. **User Account** must be set up in the **Domain**
#. **Active Directory** must be configured. :doc:`../active-directory`
#. **Agent** must be installed and running on endpoint

#. Go to **Policy** in top panel
#. Go to **Node Policy** in the left Policy panel
#. Find and click **Default Policy** to use this policy (*You can create a custom policy*) :doc:`/controlling/policy-nodegroup`
#. Find **Authentication Policy** section. Select **Active Directory** from drop-down for Federated Authentication
#. Enter **AD Domain Name** when Domain Name (AD) option becomes available
#. Click **Update**
#. Endpoint devices should be logged into the **Domain**