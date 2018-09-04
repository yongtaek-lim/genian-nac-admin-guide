Controlling Network Interface
=============================

You can control wired and wireless network interfaces on end users Windows devices by disabling wired, 
wireless, bridged, and promiscuous mode. You can also send interface disabled event notifications with 
custom messages that appear as pop-ups

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Control Network Interface** in the Agent Action window
#. Enter in **Conditions**, optional settings

Under **Disabling Network**

#. For **Network Type**, specify the Network type to be disabled (*Wired, Wireless, or both*)
#. For **Exceptions**, turn on to enable the exclusion of specified Network Devices
#. For **Disabling Network Bridge**, turn on to disable any Network Bridge Interface regardless of the exclusion above
#. For **Disabling Promiscuous**, turn on to disable any Promiscuous Interfaces regardless of the exclusion above
#. For **Interface Disabled Event Notification**, optional messages sent to user from Interface Disabled Events

Under **Enforcing Network Device Properties**

#. For **Internet Connection Sharing**, select to disable the shared Internet Connection
#. For **IPv6**, select to disable the IPv6 Interface Connection
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Network Interface** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
