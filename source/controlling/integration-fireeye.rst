Integration Guide of FireEye
============================

This guide provides an overview of integration via FireEye. It includes the following information:

   -  `1. About This Guide`_
   -  `2. Deployment of Genian NAC using FireEye`_
   -  `3. Configuring FireEye for integration via SYSLOG`_

**1. About this Guide**
-----------------------

The guide describes how to integrate with Genian NAC and FireEye.

When a specific anomaly is detected by FireEye, FireEye sends anomaly information detected to Genian NAC through SYSLOG
Genian NAC will be able to prevent the spread of anomalies by quarantine the anomaly target.

**2. Deployment of Genian NAC using FireEye**
---------------------------------------------

.. image:: /images/Integration_FireEye.jpg
   :width: 600px

#. FireEye detect the threaten device.
#. FireEye sends the anomaly information to Genian NAC via SYSLOG.
#. Genian NAC quarantines the threaten device and then Threaten device can't connect to another network.

**3. Configuring FireEye for integration via SYSLOG**
-----------------------------------------------------

**3.1 Configuration of Genian NAC**

Genian NAC receives the SYSLOG which is notification of Threaten device from FireEye
So, We need the setting on Genian NAC.
Complete the following steps to receive data from FireEye using CEF:

#. Login into Genian NAC with the administrator account
#. Go to the **Preferences** tap on the top panel.
#. Go to the **General** > **Log** on the left panel.
#. **Add** the Filter in **Syslog Options** in the middle of the center
#. Enter the content

+-----------+--------------------------+
|Name       | FireEye                  |
+-----------+--------------------------+
|Type       | host                     |
+-----------+--------------------------+
|Type Value |[IP address of FireEye]   |
+-----------+--------------------------+
|IP Prefix  |src=                      |
+-----------+--------------------------+
|MAC Prefix |smac=                     |
+-----------+--------------------------+

6. Click the **Add** button below and **Update** button

**3.2 Configuration of FireEye**

The FireEye appliances are very flexible regarding Notification output and support the following formats.

- CEF
- LEEF
- CSV

For our guide, we will use CEF
Complete the following steps to send data to Genian NAC using CEF:

#. Log into the FireEye appliance with an administrator account
#. Go to the **Settings** tap on the top panel.
#. Go to the **Notifications** on the left panel
#. Click the **rsyslog** on the middle of the center
#. Check the “Event type” in the check box
#. Make sure **Rsyslog settings** are

code ::bash

   - Default format: CEF
   - Default delivery: Per event
   - Default send as: Alert

7. **Add Rsyslog server** on the middle of under > Enter the **Name** Genian NAC > Click on **Add Rsyslog Server** button
8. Enter the IP address of the Genian NAC in the IP Address field
9. Click the **Update** button below

**3.3 Verification**

Complete the above steps
Genain NAC can receive the SYSLOG message from FireEye.

#. Go to **Log** on the top panel.
#. If It will show the Log message, **LogID** is FireEye
