Understanding Threat Detection
==============================

**Network Sensor** listens for abnormalities in network traffic and identifies endpoints with 
**Threats** and blocks them based on your access policies. You can configure Threat Definitions 
to detect abnormal network traffic such as **Ad Hoc Networks, ARP Bomb, ARP Spoofing, MAC+IP Clones,** and more.

ARP Spoofing
------------

While ARP Poisoning is a technology used to block communication of network devices, ARP Spoofing is mainly used in malicious codes 
and is used for eavesdropping communication of other parties. Genian NAC can detect ARP packets through a network sensor to detect 
devices attempting to be spoofed.

In addition, it provides a function to block devices that attempted spoofing and to return to normal MAC through ARP cache detox.

MAC/IP Cloning
--------------

The IP protocol uses IP and MAC addresses to identify the destination of the communication. Since there is no verification procedure 
at this time, it is easy to steal. If you have cloned the MAC / IP of the malicious device on the network, it is very difficult to check 
the normal system and the stolen system at the packet level.

However, Genian NAC can detect MAC / IP theft in a variety of ways. The network sensor periodically sends an ARP request to check the 
operation status of the device. If two replies are received at the same time, suspend the MAC / IP clone and designate the node as a 
critical node. In addition, if the user changes the MAC on the endpoint where the Agent is installed and the MAC is already being used by 
another device, the device is designated as a critical node.

In addition, Genian NAC provides industry-leading platform detection to detect when a node is changing to another platform, allowing 
administrators to see when changes are made, and to block devices when unauthorized platform changes are detected.

ARP Bombing
-----------

While the network sensor is monitoring ARP, it detects a device that generates excessive ARP packets and designates it as a critical node. 
It detects abnormal ARP behavior and prevents attempts to disable network access or disable network access control.

Port Scanning
-------------

Detect any device try to scan TCP or UDP ports. Genian NAC use honeypot IP for detecing scanning device.

Ad Hoc Network Connected
------------------------

Detects direct client-to-client communication

Invalid Gateway Used
--------------------

Detects a Node having an Invalid Gateway set