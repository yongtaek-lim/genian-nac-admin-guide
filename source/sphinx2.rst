Sphinx Documentation System How To
==================================

Preparation
-----------

**GitHub Account**

Signup at `GitHub`_

**Fork Main Repository**

   - Visit https://github.com/genians/genian-nac-admin-guide
   - Click Fork Icon top right
   - Your forked repo https://github.com/USERNAME/genian-nac-admin-guide

**Make local repository on your PC**

   - If you use Windows, you need to install the git
   - `Download Git`_ 

.. image:: /images/Git-Download.PNG
   :width: 500px
   
**Open Command Prompt enter following:**

.. code:: bash
   
 # git clone https://github.com/USERNAME/genian-nac-admin-guide
 # git remote add upstream https://github.com/USERNAME/genian-nac-admin-guide


**Install Sublime Text on your PC**

   - If you use Windows you need to install Python
   - Go to `Python`_ to download


**Import Project**

   - Select File > Open Folder
   - Select your source directory “genian-nac-admin-guide”


Editing contents using Sublime Text
------------------------------

**Create New Folder for Files**

   - Right Click on >source > New Folder
   - Folder Name should be one word in lowercase that best describes section
   
**Create New File within Folder**

   - Right click on desired folder > New File
   - Filename should be lowercase, and a hyphen between words. .rst must follow the name. (*e.g. some-name.rst*)

**Sample Page Formatting**

.. code:: bash

 (Header) <Some Title>
 =====================
 <Space Needed>
 (Intro) <Some Intro>
 <Space Needed>
 (Sub-Title) <To Do Something>
 -----------------------------
 <Space Needed>
 #. <Go to somewhere and do something>
 #. <Next Step>
 <Space Needed>
    -  <Sub-step>
    -  <Sub-step>
    -  <Sub-step>
    -  <Sub-step>    
 <Space Needed>
 #. <Next Step>
 
**Add Images To File**

   - Copy image files from local machine to Eclipse images folder
   - Add code for images where you would like your image to be
   
.. code:: bash

 .. image:: /images/some-image.PNG
    :width: 500px
 
**Add Table To File**

.. code:: bash 

 +-----------+-----------+-----------+
 |1st Column |2nd Column |3rd Column | <-----Title Block
 +===========+===========+===========+ 
 |           |           |           |  <-----First Data Block
 +-----------+-----------+-----------+ 

**Add CLI Coding Box**

.. code:: bash

 .. code:: bash
 <Space Needed>
  Lines of Code with no spaces to follow (*Single space before "Lines" needed)
  
**Compile Document**

   - Press Ctrl-B within the editor and see changes and errors in Console on right
   - Generated HTML will be placed under genian-nac-admin-guide/build/html directory
   - Open index.html page to review and verify changes 

(*e.g.  file:///C:/Users/Bill%20Eaton/genian-nac-admin-guide/build/html/index.html*)

**If you change any doctree:: or add new pages, it will require to clean build**

   - Select Project > Clean
   - Press Ctrl-B

Apply your change to main repository
------------------------------------

**Commit and Push to your repo**

   - Right click on Top of Project Explorer
   - Select Team > Commit
   - Make sure your change file on Staged Changes
   - Add a “Commit Message”
   - Click “Commit and Push” button

.. image:: /images/eclipse-commit.PNG
   :width: 500px
 
.. image:: /images/eclipse-commit-push.PNG
   :width: 500px

Stay current with Main Repo changes
-----------------------------------
      
**Update main repo changes to your local repo**

   - Right click on Top of Project Explorer
   - Select Team > Pull (second one)
   - Change Remote from “origin” to “upstream”
   - Click “Finish”

.. image:: /images/eclipse-2ndpull.PNG
   :width: 500px
   
.. image:: /images/eclipse-pull.PNG
   :width: 500px
   
**Make Pull Request**

   - Visit your repo on GitHub (*https://github.com/USERNAME/genian-nac-admin-guide*)
   - Click “New Pull request”

(*Main repository moderator will approve changes, or ask you to make some suggested changes*)

.. _GitHub: https://github.com/
.. _Download Git: https://git-scm.com/download/win
.. _Python: https://www.python.org/downloads/release/python-365/
.. _Eclipse: https://www.eclipse.org/downloads/
