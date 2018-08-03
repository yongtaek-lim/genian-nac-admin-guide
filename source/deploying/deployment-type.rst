Deployment Type
===============

On-Premises
-----------

**Policy Server** and **Network Sensor** can be deployed one of two ways

   -  Policy Server/Network Sensor combined
   -  Policy Server and Network Sensor separated
   
The switch port can be a standard connection or can be a trunked port for up to 128 VLANs. If your location has more than 128 VLANs then a second Network Sensor would be required
(*If you have 2 Network Sensors on the same network or overlapping networks in an 802.1q environment you will have duplicate nodes. There is no harm in having duplicated nodes, it is just something to be aware of.*)

Policy Server and Network Sensor Combined

.. image:: /images/Deploying-PolicyServer-NetworkSensor-Combined.png
   :width: 850px

Policy Server and Network Sensor Separated

.. image:: /images/Deploying-PolicyServer-NetworkSensor.png
   :width: 850px

Cloud-Managed
-------------

**Policy Server** can be deployed in the Cloud, while **Network Sensors** can be deployed by connecting them to an Edge Switch at your Remote Site locations.  The Edge Switch ports can be a standard connection or can be trunked ports for up to 128 VLANs. If your location has more then 128 VLANs then a second **Network Sensor** would be required

.. image:: /images/Deploying-PolicyServer-NetworkSensor-Cloud.png
   :width: 850px
