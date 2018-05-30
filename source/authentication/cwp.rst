Configuring User Authentication by Captive Web Portal
=====================================================

Genian NAC uses a **Captive Web Portal** (**CWP**) for Guest Access, Authentication, Information, and Instructions to become compliant with enforced policies. You can configure the Policy Server to redirect both users and guests to a **CWP login** page for **Authentication**. Users are then forced to enter Username and Password to authenticate against a database before being allowed access to the network. This allows you to identify users behind endpoint devices, and present them with information or login instructions.

To Edit “User Not Authenticated” Status Group
---------------------------------------------

#. Go to **Policy** in top panel
#. Go to **Group > Node** in the left Policy panel
#. Find and click on **User Not Authenticated** in the Node Group window
#. Find **General/Application Mode** section and select **Enable**
#. Click **Update**
#. Click **Apply** in top right corner

Apply “User Not Authenticated” Status Group to “User Not Authenticated” Enforcement Policy
------------------------------------------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Find and click on **User Not Authenticated** Enforcement Policy
#. Find **General/Application Mode** section and select **Enable**
#. Find **Node Group** section and verify **User Not Authenticated** is added (*If not then click Assign and add it in*)
#. Click **Update**
#. Click **Apply** in top right corner

(*Navigate to /cwp and you should now see the Authentication Login icon on the page*)
