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

.. image:: /images/Git-Download.png
   :width: 500px
   
**Open Command Prompt enter following:**

.. code:: bash
   
 # git clone https://github.com/USERNAME/genian-nac-admin-guide
 # git remote add upstream https://github.com/USERNAME/genian-nac-admin-guide


**Install Sphinx on you PC**

   - If you use Windows you need to install Python
   - Go to `Python`_ to download

**Open Command Prompt enter following:**

.. code:: bash
 
 # pip install Sphinx
 # pip install sphinx_rtd_theme


Editing contents using Eclipse
------------------------------

**Install Eclipse**

   - Go to `Eclipse`_ to download

**Install additional package on Eclipse**

   - Go to Help > Eclipse Marketplace
   - Search ‘CDT’ and click “install” on “The Complete Eclipse C/C++ IDE”
   - Search ‘rest’ and click “install” on ReST Editor”

.. image:: /images/CDT-install.png
   :width: 500px

.. image:: /images/rest-install.png
   :width: 500px

**Import Project**

   - Select File > Import
   - Select Existing Code as Makefile Project under C/C++
   - Click “Next”
   - Project Name is “Admin Guide”
   - Select your source directory “genian-nac-admin-guide”
   - Click “Finish”   
                                                                       
.. image:: /images/Makefile-Project.png
   :width: 500px

.. image:: /images/genian-nac-admin-guide.png
   :width: 500px
   
**Change project settings**

   - Select Project > Properties
   - Select “C/C++ Build” on left menu
   - Select “Behavior” Tab
   - Change value of Build “all” -> “html”
   - Click “Apply and Close”

.. image:: /images/Eclipse-project-properties.png
   :width: 500px

**Compile Document**

   - Press Ctrl-B on editor
   - Generated HTML will place under genian-nac-admin-guide/build/html directory
   - Open index.html  

(*e.g.  file:///C:/Users/Bill%20Eaton/genian-nac-admin-guide/build/html/index.html*)

**If you change any doctree:: or add new page would require to clean build**

   - Select Project > Clean
   - Press Ctrl-B

**Commit and Push to your repo**

   - Right click on Top of Project Explorer
   - Select Team > Commit
   - Make sure your change file on Staged Changes
   - Add a “Commit Message”
   - Click “Commit and Push” button

**Update main repo changes to your local repo**

   - Right click on Top of Project Explorer
   - Select Team > Pull (second one)
   - Change Remote from “origin” to “upstream”
   - Click “Finish”

.. image:: /images/eclipse-2ndpull.png
   :width: 500px
   
.. image:: /images/eclipse-pull.png
   :width: 500px

Apply your change to main repository
------------------------------------

**Make Pull Request**

   - Visit your repo on GitHub (*https://github.com/USERNAME/genian-nac-admin-guide*)
   - Click “New Pull request”

(*Main repository moderator will approve changes, or ask you to make some suggested changes*)

.. _GitHub: https://github.com/
.. _Download Git: https://git-scm.com/download/win
.. _Python: https://www.python.org/downloads/release/python-365/
.. _Eclipse: https://www.eclipse.org/downloads/
