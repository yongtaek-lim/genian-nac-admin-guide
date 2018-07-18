Installing Windows Agent
========================

You can install **Agent** on Windows devices through GPO, Captive Web Portal (CWP), or manually using removable storage media

Install Windows Agent
---------------------

#. Download Agent

   -  https://(*IP or FQDN*)/agent

#. Choose Agent: DO NOT change the filename to avoid name conflicts
  
   -  Windows installer version: GnUpdate_(*IP or FQDN*).exe

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
