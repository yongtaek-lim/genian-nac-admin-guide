Configuring User Authentication by AD Domain Login
==================================================

You can configure the **Policy Server** to integrate with Active Directory Domain Login for User Authentication

To Configure User Authentication by AD Domain Login
---------------------------------------------------

#. A **Domain** must be configured in Active Directory
#. **User Account** must be set up in the **Domain**
#. **Active Directory** must be configured. `Configuring Active Directory`_
#. **Agent** must be installed and running on endpoint
#. Go to **Policy** in top panel
#. Go to **Node Policy** in the left Policy panel
#. Find and click **Default Policy** to use this policy (*You can create a custom policy*) `Creating Enforcement Policy for Node Group`_
#. Find **Advanced: Authentication Policy** section. Select **Active Directory** from drop-down for Federated Authentication
#. Enter **AD Domain Name** when Domain Name (AD) option becomes available
#. Click **Update**
#. Endpoint devices should be logged into the **Domain**

To Verify AD Domain Login
-------------------------

#. Go to **Management > Node** in top panel
#. Find and click **IP Address** of Endpoint
#. Go to the **General** tab. Find **Domain** (*You should see the Domain this endpoint is logged into*)

.. _Configuring Active Directory: https://www.genians.com/docs/administrators-guide/?section=configuring-active-directory
.. _Creating Enforcement Policy for Node Group: https://www.genians.com/docs/administrators-guide/?section=creating-enforcement-policy-node-group
