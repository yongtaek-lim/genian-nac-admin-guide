Customizing CWP Design
======================

Customizing the **Captive Web Portal** page allows you to edit the current Default page, create something completely new, or add logos from current companies web page. This gives you the ability to display the same look and feel as your current internal web pages for your end users.
Under **Preferences > Captive Web Portal > Page Design**
Four tabs will be displayed to allow you to customize your CWP page

- **Page** tab allows you to edit current default page
- **Custom Page** tab allows you to customize your own CWP page
- **Text Contents** tab allows you to add various text messages
   - **Authentication Page Help Message**
   - **User Account Request Page Message**
   - **Active-X Control Message**
   - **Authentication Box Message**
   - **User Verification Message**
- **Image** tab allows you to upload custom images to make CWP look and feel like your own

Customize Default Captive Web Portal Page Design
------------------------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Captive Web Portal > Page Design** in the left Preferences panel
#. Find and click **Page** tab
#. You can edit **Header**, **Body**, and **Footer** using supported **HTML**, **CSS**, and **JavaScript**
#. Find and click **Image** tab. Select Image file to upload and use in **Page** tab in the **Header** field
#. Click **Update**

.. code:: bash

   <strong>SAMPLE</strong>
   <table border="0" cellpadding="0" cellspacing="0" bgcolor="#ffffff">
   <tr height="0"> 
      <td width="50%"></td>
      <td width="625" align="center"><img src="/custom/logo.jpg" border="0" align="">
      </td>
   <td width="50%"></td>  
   </tr>
   </table>

Create Your Own Custom CWP Page
-------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Captive Web Portal > Page Design** in the left Preferences panel
#. Find and click **Custom Page** tab
#. You can edit **Custom Page** field using supported **HTML**, **CSS**, and **JavaScript**
#. Click **Update**

Check and Verify Page Changes
-----------------------------

#. Find and click **Preview** button for either **Default CWP Page** or **Custom CWP Page**

Add Custom CWP Page In A Enforcement Policy
-------------------------------------------

#. Go to **Policy** in the top panel/li>
#. Go to **Enforcement Policy** in the left Policy panel
#. Find and click **name of Enforcement Policy**
#. Find **Enforcement Options**: **Captive Web Portal** section and select **Custom URL** in **Redirecting to** drop-down
#. Add **URL** or **Use Template** (*e.g. URL = http://[Policy server IP]/custom/cwp.html*)
