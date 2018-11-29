Creating Permissions
====================

Understanding Permissions
-------------------------

Permissions allow you to define Node Access based off of a combination of various objects to include Network, Service, and Time.
Out of the box Genians has 2 Permissions that are used in our pre-defined Enforcement Policies. These are **PERM-ALL** and **PERM-DNS**. 

  - **PERM-ALL**: Allow all services on all networks
  - **PERM-DNS**: Only allow DNS service on all networks

(*You can create custom Permissions but you first need to understand about the Network, Service and Time objects and how to edit and create them*)

  - **Network**  - A rule that identifies certain networks and allows you to define access based off of IP/Netmask or IP Range.
  - **Service**  - A rule that identifies services to allow you to define access through several protocols and ports.
  - **Time**  - A rule used to create different access times to either allow during certain days and hours, or deny during certain days or hours.

(*Exclude checkbox is used to as a **NOT Operator**. e.g. For a defined Network, checking the box for Exclude allows Nodes to access ALL networks other then this one*)

.. important:: Permission is applicable only to ARP Poisoning and Port Mirroring enforcement.

Step 1. Create A Custom Network Object
--------------------------------------

#. Go to **Policy** in top panel
#. Go to **Object > Network** in left Policy panel
#. Click **Tasks > Create**
#. Enter the following:

   - **ID**: Unique-Name  (*e.g. Guest Network*)
   - **Group**: Select Group or Groups to apply to this Network Object
   - **Network IP**: IP/Netmask or Range

#. Click **Create**
#. Click **Apply**

Default Network Objects
-----------------------

- **@LOCAL** - Is an object representing the local network of each intended sensor interface. A local server can be accessed by anyone on the local network but outside access is denied.
- **@MANAGED** - Is combined networks from ALL Network Sensors. If New Network Sensors are added then those networks are automatically added and included into the @MANAGED group.

Example:

+----------------+------------------+
|Network Sensor  |IP Address        |
+================+==================+ 
|Sensor 1        |192.168.10.10     |
+----------------+------------------+  
|Sensor 2        |192.168.20.10     |
+----------------+------------------+
|Sensor 3        |192.168.30.10     |
+----------------+------------------+

A Node connects with IP: 192.168.10.100

If the Node is allowed and the Network object is LOCAL
Group: A(192.168.10.100)
Perm Destination Network: Local
The node can only connect to the Network range 192.168.10.0/24

The Node is allowed and the Network object is MANAGED
Group:A(192.168.10.100)
Perm Destination Network: Manage
The node can  only connect to the Network ranges in 192.168.10.0/24, 192.168.20.0/24, 192.168.30.0/24


Step 2. Create A Custom Service Object
--------------------------------------

#. Go to **Policy** in top panel
#. Go to **Object > Service** in left Policy panel
#. Click **Tasks > Create**
#. Enter the following:

   - **ID**: Unique-Name  (*e.g. Port 80*)
   - **Group**: Select Group or Groups to apply to this Network Object
   - **Service Port**: Select a Protocol and Operator to choose ports (*e.g. For Port 80: TCP/ = 80, and TCP/ = 8080*)
      
#. Click **Update**
#. Click **Apply**

Step 3. Create A Custom Time Object
-----------------------------------

#. Go to **Policy** in top panel
#. Go to **Object > Time** in left Policy panel
#. Click **Tasks > Create**
#. Enter the following:

   - **ID**: Unique-Name  (*e.g. Business Hours for Guests*)
   - **Group**: Select Group or Groups to apply to this Network Object
   - **Time**: Specific Date or Range of Days and Hours (*e.g. Time: 0800-1800, Days: Monday-Friday*)
            
#. Click **Create**
#. Click **Apply**

Step 4. Create A Permission
---------------------------

#. Go to **Policy** in top panel
#. Go to **Object > Permission** in left Policy panel
#. Click **Tasks > Create**
#. Enter the following:

   - **ID**: Unique-Name
   - **Description**: Some description to help understand what the Permission does
   - **Settings**: Select and edit Network, Service, and Time 
   - **Exclude**: Is used as a NOT Operator
         
#. Click **Create**
#. Click **Apply**
