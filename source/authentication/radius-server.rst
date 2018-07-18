Configuring RADIUS Server
=========================

You can configure Policy Server to integrate with Radius Server for User Authentication

Enable Policy Server through CLI RADIUS Server
----------------------------------------------

#. Log in to **CLI** and **Enable Radius Server** feature
#. Get into configuration mode (**configure terminal**)
#. Enter **Interface** to apply **Radius Server** to and **Enable**
#. Then **Exit**

CLI Command to enable radius-server on interface

.. code:: bash

configure terminal
interface eth0.55 radius-server enable
exit

Configure RADIUS Server Service
-------------------------------

#. Login into your device **https://<IP Address>/mc/**  (*See Connecting Administrator Management Interface*)
#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. In the **RADIUS Server** section enter in the following:

   - **Shared Secret Key** (*Must be 9-30 characters*)
   - **RADIUS Client IP** would be **IP Address of Wireless Access Point**
   - Leave **Server Port** as **1812** for Authentication
   - **EAP Authentication** select **On** from drop-down
   - Select **EAP Type** as **GTC** from drop-down
   - **MAC Authentication** set to **Off**
   - **Accounting** select **On** from drop-down

#. Use EAP GTC for SecurID 2 Factor authentication
#. If using AD authentication, select to use MSCHAPv2 and enter an AD Account for Genian NAC to authenticate against

   - Enable Genian NAC Account
   - Enable AD Account
   - Domain Name
   - Username
   - Password

#. Click Update

Configure RADIUS Authentication
-------------------------------

#. Login into your device **https://<IP Address>/mc/**  (*See Connecting Administrator Management Interface*)
#. Go to **Preferences** in the top panel
#. Go to **User Authentication > Authentication Integration** in the left Preferences panel
#. In the **RADIUS Authentication** section enter in the following:

   - **Server Address** would be **IP Address of Wireless Access Point**
   - Leave **Server Port** as **1813**
   - **Federated Authentication** select **On** from drop-down
   - **Shared Key**  (*Must be 9-30 characters*)
   - **Packet Type** should be Checked for both **Start** and **Stop**
   - **Detection Methods** select **MAC** from drop-down
   - **Scope** select **All Nodes** from drop-down

#. Click Update
