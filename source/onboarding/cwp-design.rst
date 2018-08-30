Customizing CWP Design
======================

Customizing the **Captive Web Portal** page allows you to edit the current Default page, create something completely new, or add logos from current companies web page. This gives you the ability to display the same look and feel as your current internal web pages for your end users.
Under **Preferences > Captive Web Portal > Design Template**
Four tabs will be displayed to allow you to customize your CWP page

- **Component Options**: tab allows you to edit the page using the component.
- **Edit**: tab allows you to customize your own CWP page
- **CSS Style**: tab allows you to add CSS Style
- **Layout**: tab allows you to edit page layout 
- **Image**: tab allows you to upload custom images to make CWP look and feel like your own

Component Options
-----------------

#. Click the add or delete button for the required component
#. Page preview on Main page in the right side of the Webconsole
#. Click **Update**

Edit
----
#. CWP page display in html code form
#. Provide pages in html code format

- Modify the page by adding or removing the tag of the component to the code
- Can be modified using html code

3. Click **Update**
4. Page preview on Main page in the right side of the Webconsole

CSS Style
---------
You can define CSS Style class and use it in EDIT Tab or Layout Tab.

1. Input the CSS style code in "CSS Style" tab.

>>> .test {color:red;}

2. To use defined CSS style in "Edit" tab

>>> <div class="test">
TEST
</div>

3. Click **Update**
4. Page preview on Main page in the right side of the Webconsole


Layout
------
You can modify the layout of the page using Html code.

>>> <?xml version='1.0' encoding='UTF-8' ?> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:ui="http://xmlns.jcp.org/jsf/facelets"
      xmlns:h="http://xmlns.jcp.org/jsf/html"
      xmlns:p="http://primefaces.org/ui"
      xmlns:gncomponent="http://xmlns.jcp.org/jsf/composite/gncomponent">
$HEAD
<body id="body1">
    $PAGEHEADER
    <div id="wrap" class="wrap">
        $CUSTOMPAGEHEADER
        <div id="content" class="content">
            <!-- Don't delete code -->
            $CONTENT
            <!-- Don't delete code -->
        </div>
        $CUSTOMPAGEFOOTER
    </div>
</body>
</html>

Image
-----
upload custom images to make CWP look and feel like your own

.. note:: Upload an image file for CWP page. The file name must contain only alphabets and Select an image file to upload (jpg/gif/png only)

Apply the defined CWP template
------------------------------
#. Go to **Policy** in the top panel/li>
#. Go to **Node Policy** in the left Policy panel
#. Find and click **name of Node Policy**
#. Find **CWP Design Template** in the main **Management Policy**
#. Select a Design Template for a CWP page
#. Click **Update** and **apply** on the right top panel.


