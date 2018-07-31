Enabling MAC Authentication
===========================
 
The MAC authentication feature is a mechanism by which incoming traffic originating from a specific MAC address is forwarded only if the source MAC address is successfully authenticated by a RADIUS server. The MAC address itself is used as the username and password for RADIUS authentication. The user does not need to provide a specific username and password to gain access to the network

- If RADIUS authentication for the MAC address is successful, traffic from the MAC address is forwarded in hardware
- If the RADIUS server cannot validate the user’s MAC address, then it is considered an authentication failure, and a specified authentication-failure action can be taken

Enable MAC Authentication
-------------------------

#. Go to **Preferences** in the top panel
#. Go to **Service > RADIUS Server** in the left Preferences panel
#. Find **RADIUS Server > MAC Authentication** section in the RADIUS Server window. Enter the following:

   - Enable **MAC Authentication** from drop down
   - Select proper option from the **Node Group** drop down

#. Click **Update**
