Configuring Windows Settings
============================

Policy Server communicates with the Agent to configure the Windows Security Settings on end users Windows devices. You can disable Guest Accounts, turn on Windows Firewall, block specific inbound ports (e.g. UDP/5355), turn off Remote Desktop, control Autorun settings, and setup sync with NTP

To See the Configuration of the Plugin
--------------------------------------

- Go to **System > Update > Genian Software > Plugin > Configure Windows Settings**

To Add the Agent Action to a Policy
-----------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Configure Windows Settings** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**

To Configure Windows Settings
-----------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Configure Windows Settings** in the Agent Action window
#. Enter in **Conditions**, and adjust **Agent Actions** based off of your network requirements
#. Click **Update**
