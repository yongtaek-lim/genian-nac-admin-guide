Understanding Anomaly Detection
===============================

**Network Sensor** listens for abnormalities in network traffic and identifies endpoints with 
**Anomaly** and blocks them based on your access policies. You can configure Anomaly Definitions 
to detect abnormal network traffic such as **Ad hoc Network, ARP Bomb, Spoofed ARP, MAC+IP Clones,** and more.


ARP Bomb
--------

While the network sensor is monitoring ARP, it detects a device that generates excessive ARP packets and designates it as a critical Node. 
It detects abnormal ARP behavior and prevents attempts to disable network access or disable network access control.
An attacker Node continually keeps sending request packets to the target Node, thereby causing its cache to fill up quickly. 
Soon the target Node will spend more of its resources to maintain its cache, which may lead to buffer overflow. 
And real mapping would never be entered in the cache. 

MAC+IP Clones
-------------

The IP protocol uses IP and MAC addresses to identify the destination of the communication. Since there is no verification procedure 
at this time, it is easy to steal. If you have cloned the MAC / IP of the malicious device on the network, it is very difficult to check 
the normal system and the stolen system at the packet level.

However, Genian NAC can detect MAC / IP theft in a variety of ways. The network sensor periodically sends an ARP request to check the 
operation status of the device. If two replies are received at the same time, suspend the MAC / IP clone and designate the Node as a 
critical Node. In addition, if the user changes the MAC on the endpoint where the Agent is installed and the MAC is already being used by 
another device, the device is designated as a critical Node.

In addition, Genian NAC provides industry-leading platform detection to detect when a Node is changing to another platform, allowing 
administrators to see when changes are made, and to block devices when unauthorized platform changes are detected.

Multi-Homed / Ad hoc Network
----------------------------

Detects direct client-to-client communication (*Agent required*)

Port Scanning
-------------

Detect any device try to scan TCP or UDP ports. Genian NAC use honeypot IP for detecing scanning device.

Rogue Gateway
-------------

Detects a Node having a rogue gateway configured (*Agent required*)

Sensor MAC Clones
-----------------

Detects whether a Sensor MAC address is cloned (*No configuration settings required*)

Spoofed ARP
-----------

While ARP Poisoning is a technology used to block communication of network devices, ARP Spoofing is mainly used in malicious codes 
and is used for eavesdropping communication of other parties. Genian NAC can detect ARP packets through a network sensor to detect 
devices attempting to be spoofed.

In addition, it provides a function to block devices that attempted spoofing and to return to normal MAC through ARP cache detox.

Unauthorized Service Request
----------------------------

Detects the service that are not authorized but requested