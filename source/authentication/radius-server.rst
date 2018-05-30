Configuring RADIUS Server
=========================

You can configure Policy Server to integrate with Radius Server for User Authentication

To Configure Policy Server to Integrate with RADIUS Server
----------------------------------------------------------

Log in to **CLI** and **Enable Radius Server** feature
Get into configuration mode (**configure terminal**)
Enter **Interface** to apply **Radius Server** to and **Enable**
Then **Exit**
CLI Command to enable radius-server on interface

configure terminal
interface eth0.55 radius-server enable
exit

configure terminal
interface eth0.55 radius-server enable
exit

Login into your device https://<IP Address>/mc/  (*See Connecting Administrator Management Interface*)
Go to Preferences in the top panel
Go to Service > RADIUS Server in the left Preferences panel
In the RADIUS Server section enter in the following:
Shared Secret Key
RADIUS Client IP
Leave Server Port as 1812
Turn On EAP Authentication
Select EAP Type
MAC Authentication
Accounting
Use EAP GTC for SecurID 2 Factor authentication
If using AD authentication, select to use MSCHAPv2 and enter an AD Account for Genian NAC to authenticate against
Enable Genian NAC Account
Enable AD Account
Domain Name
Username
Password
Click Update
