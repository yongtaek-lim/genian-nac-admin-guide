Installing Windows Agent
========================

You can install **Agent** on Windows devices through GPO, Captive Web Portal (CWP), or manually using removable storage media

Install Windows agent
---------------------

- `Download and install via agent download page`_
- `Installing the agent via CWP after applying the Genian NAC agent enforcement policy`_
- `MSI packages for installation via Active Directory GPOs`_
- `Verify Windows Agent installed`_
- `Where To Find Agent Logs On Windows Device`_

Download and install via agent download page
--------------------------------------------

#. Download Agent

   -  https://(*IP or FQDN*)/agent

#. Choose Agent: DO NOT change the filename to avoid name conflicts
  
   -  Windows installer version: GnUpdate_(*IP or FQDN*).exe

.. note:: If the user does not have the file installation permission, the installer can not be executed, so Need to run with administrative privileges with file install permissions


Installing the agent via CWP after applying the Genian NAC agent enforcement policy
-----------------------------------------------------------------------------------

Genian NAC policy is created to provide agent install button via CWP for network access when the agent is not installed
In the CWP message, click the Install Agent button to download and install the Agent

To apply the  "Agent install" policy option

#. Go to **Policy** in the top panel
#. Go to **Node Policy**
#. Click "Node policy ID" where do you want to apply the policy.
#. Find the **Agent Policy** section
#. Select **Agent** and  **on** in the checkbox

.. note:: Nodes in the node group assigned to the node policy will see the "Agent Install button" on the CWP connection page when the agent is not installed.

MSI packages for installation via Active Directory GPOs
-------------------------------------------------------

If you need an Agent MSI file for deployment, you need to input the following information through Slack and request it
- Customer
- Agent Version
- Policy server IP

How to deploy the Agent MSI via Active Directory GPOs

.. note:: If the user has AD User privilege, the Agent may not operate properly and the Agent Execution Account must be modified.

#. Go to **Policy** in the top panel
#. Go to **Node Policy**
#. Click "Node policy ID" where do you want to apply the policy.
#. Find the **Agent Policy** section
#. Select **Execution Account** and "Local System Account: in the checkbox
#. Enter the "Username" and "Password"

.. note:: Username is qualified the Administrator authority account in Active Directory if not Agent is not runnning well

6. How to set up to deploy the MSI Package via AD 
 
.. toctree::
   :maxdepth: 1

   deploy-msi-agent

Verify Windows Agent installed
------------------------------

#. Select **Management > Node**
#. Click **NT AG SS** column in Nodes window (*If a node has an installed Agent, the Agent icon will show*)

Genian Agent Options On Windows Device
--------------------------------------

#. Go to **Systray** of Windows device
#. Find and right-click on **Genians Agent Icon**
#. Listed options allow you to do the following:

   -  **Read Notice:** Shows current notices from the Administrator
   -  **Read Message:** Shows current messages from the Administrator
   -  **View My Status:** Shows the devices current **Captive Web Portal (CWP)** page
   -  **Login (L):** Allows user to log in and upon successful login displays CWP page
   -  **Logout (O):** Allows user to log out
   -  **View User Information:** Allows user to view account information upon successful login
   -  **View Network Connections:** Allows user to view the devices active network connections
   -  **View USB Information:** Allows user to view the devices USB information
   -  **Delete Agent:** (*User is unable to delete the installed Agent. This must be done by the Administrator*)
   -  **About Genian Agent:** Allows user to see current information about installed Agent

Where To Find Agent Logs On Windows Device
------------------------------------------

#. Open **File Explorer** on Windows device
#. Go to **C:\Program Files\Geni\Genian\Logs**
#. Sort by **Date modified**
