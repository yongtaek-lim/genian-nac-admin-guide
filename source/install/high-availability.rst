Configuring Policy Server for High Availability
===============================================

Genians can be set up using two Appliances in a active/passive configuration, one acting as a primary while the other as a secondary. 
These two Appliances communicate with each other to synchronize data and will failover from one to the other in the event of a system failure.

- **Group** – VRRP Group ID
- **Linkupdelay** – Time to wait until interface is activated
- **No-Virtual-Mac** – Does not convert MAC Address info to Virtual-MAC when switching to Master
- **Nopreempt** – Device as Master takes precedence regardless of priority
- **Priority** – Priority Value. Highest Value is Master
- **Timeout** – Wait time for VRRP packet loss
- **Virtual-IP** – Shared IP for devices and UI


Serial Connection to Server if SSH is not established
-----------------------------------------------------
- Protocol: **Serial**
- Port: **COM1**
- Baud Rate: **115200** (*9600 for Mini-PC*)
- Data Bits: **8**
- Parity: **None**
- Stop Bits: **1**


How to configure Policy Servers for High Availability
-----------------------------------------------------
#. Connect to each Policy Server by connecting to Command Line Interface
#. Run a show configuration to see current configuration. (*Record Master Server device-id as this needs to be the same on both Policy Servers*)
#. Enter Global Config mode: config terminal
#. On each Policy Server enter the following configurations:


Master Policy Server
--------------------
.. code:: bash

 1. Interactive Wizard
 2. Manual Configuration

 Select installation type: 2

 Enter administrator username (4-31 characters) [admin]: admin

 # Password must contain at least one alphabet, number and special character
 Enter administrator password (minimum 9 characters): *********
 Re-enter Password:

 Welcome to Genian NAC
 Username: admin
 Password:
 The privileged EXEC mode password is the same as the console login password.
 For security reasons please change your password.

 Type ‘enable’ to access privileged EXEC mode for password change.
 genian> en
 Password:

 genian(config)# hostname MASTER
 MASTER(config)# interface eth0 address 172.29.20.11 255.255.255.0
 MASTER(config)# interface eth0 gateway 172.29.20.1
 MASTER(config)# ip default-gateway 172.29.20.1
 MASTER(config)# ip name-server 8.8.8.8
 MASTER(config)# data-server username root
 MASTER(config)# data-server enable
 MASTER(config)# data-server password genian123!
 MASTER(config)# data-server access-list 172.29.20.10,172.29.20.12
 MASTER(config)# data-server replica serverid 1
 MASTER(config)# data-server replica enable
 MASTER(config)# log-server cluster-name GENIAN
 MASTER(config)# log-server enable
 MASTER(config)# log-server cluster-peers 172.29.20.12
 MASTER(config)# interface eth0 management-server enable
 MASTER(config)# interface eth0 node-server enable
 MASTER(config)# interface eth0 ha priority 200
 MASTER(config)# interface eth0 ha group 20
 MASTER(config)# interface eth0 ha linkupdelay 30
 MASTER(config)# interface eth0 ha nopreempt enable
 MASTER(config)# interface eth0 ha timeout 20
 MASTER(config)# interface eth0 ha virtual-ip 172.29.20.10

 MASTER(config)# show configuration
 cli-pass change interval 0D
 cli-pass history num 0
 cli-pass minimum age 0D

 data-server enable
 data-server password ******
 data-server replica enable
 data-server replica serverid 1
 data-server username root

 device-id xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx (*Use same device-id for both Policy Servers*)

 hostname MASTER

 interface eth0 address 172.29.20.11 255.255.255.0
 interface eth0 gateway 172.29.20.1
 interface eth0 ha group 20
 interface eth0 ha linkupdelay 30
 interface eth0 ha nopreempt enable
 interface eth0 ha priority 200
 interface eth0 ha timeout 20
 interface eth0 ha virtual-ip 172.29.20.10
 interface eth0 management-server enable
 interface eth0 node-server enable

 ip default-gateway 172.29.20.1
 ip name-server 8.8.8.8

 log-server enable
 log-server cluster-name GENIAN
 log-server cluster-peers 172.29.20.12

Slave Policy Server
-------------------
.. code:: bash

 1. Interactive Wizard
 2. Manual Configuration

 Select installation type: 2

 Enter administrator username (4-31 characters) [admin]: admin
 # Password must contain at least one alphabet, number and special character
 Enter administrator password (minimum 9 characters): *********
 Re-enter Password:

 Welcome to Genian NAC
 Username: admin
 Password:
 The privileged EXEC mode password is the same as the console login password.
 For security reasons please change your password.

 Type ‘enable’ to access privileged EXEC mode for password change.
 genian> en
 Password:

 genian(config)# hostname SLAVE
 genian(config)# device-id xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx (*From Master server*)
 SLAVE(config)# interface eth0 address 172.29.20.12 255.255.255.0
 SLAVE(config)# interface eth0 gateway 172.29.20.1
 SLAVE(config)# ip default-gateway 172.29.20.1
 SLAVE(config)# ip name-server 8.8.8.8
 SLAVE(config)# data-server username root
 SLAVE(config)# data-server enable
 SLAVE(config)# data-server password genian123!
 SLAVE(config)# data-server access-list 172.29.20.10,172.29.20.11
 SLAVE(config)# data-server replica serverid 2
 SLAVE(config)# data-server replica enable
 SLAVE(config)# data-server replica masterhost 172.29.20.11
 SLAVE(config)# data-server replica username root
 SLAVE(config)# data-server replica password genian123!
 SLAVE(config)# log-server cluster-name GENIAN
 SLAVE(config)# log-server enable
 SLAVE(config)# log-server cluster-peers 172.29.20.11
 SLAVE(config)# interface eth0 management-server enable
 SLAVE(config)# interface eth0 node-server enable
 SLAVE(config)# interface eth0 ha priority 100
 SLAVE(config)# interface eth0 ha group 20
 SLAVE(config)# interface eth0 ha linkupdelay 30
 SLAVE(config)# interface eth0 ha nopreempt enable
 SLAVE(config)# interface eth0 ha timeout 20
 SLAVE(config)# interface eth0 ha virtual-ip 172.29.20.10

 SLAVE(config)# show configuration
 cli-pass change interval 0D
 cli-pass history num 0
 cli-pass minimum age 0D


 data-server enable
 data-server access-list 172.29.20.0/24
 data-server password ******
 data-server replica enable
 data-server replica masterhost 172.29.20.11
 data-server replica password ******
 data-server replica serverid 2
 data-server replica username root
 data-server username root

 device-id xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

 hostname SLAVE

 interface eth0 address 172.29.20.12 255.255.255.0
 interface eth0 gateway 172.29.20.1
 interface eth0 ha group 20
 interface eth0 ha linkupdelay 30
 interface eth0 ha nopreempt enable
 interface eth0 ha priority 100
 interface eth0 ha timeout 20
 interface eth0 ha virtual-ip 172.29.20.10
 interface eth0 management-server enable
 interface eth0 node-server enable

 ip default-gateway 172.29.20.1

 log-server enable
 log-server cluster-name GENIAN
 log-server cluster-peers 172.29.20.11

How to test DB replication
--------------------------
.. code:: bash

 ——————MASTER—————-
 MASTER(config)# superadmin admin genian123 aa@aa.com
 MASTER# show superadmin
 admin

 ——————SLAVE—————–
 SLAVE# show superadmin
 admin
