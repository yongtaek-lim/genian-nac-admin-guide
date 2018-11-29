Configuring Agent Action For Enforcement Policy
===============================================

Enforcement Policy Agent Actions use the installed Agent to do various administrative tasks, allowing you to take various actions on endpoint devices. You can Control Network Interface, Control Power Options, Notify User, or more.

To Configure Agent Action for Enforcement Policy
------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy > Agent Action** in the left Policy panel
#. Click **Tasks > Create**
#. Click **Tasks > edit Network Sensor Settings**
#. Find **General** section and add in the following:

   - **Name** (*Some unique name that best describes the function*)
   - **Description** (*Description that best describes the function*)
   - **CWP Message** (*Optional message when user is redirected to CWP*)
   - **Label** (*Optional setting*)

#. Find **Condition** section and add in optional conditions that apply. Click **Add**

(*If Boolean Operator is set to “**AND**”, all conditions have to be met. If set to “**OR**” any of the conditions can apply*)

#. Find **Agent Action** section and configure the following options:

   - **OS Type** (*Windows, Linux, macOS, Android*)
   - **Plugin** (*Windows example*)
   
      - **Control Network Interface** has various control settings of all Network Interfaces
      - **Control Power Options** allows you to control various Power Options of the Windows machine
      - **Notify User** allows you to notify user and keep them informed of the current Enforcement Policy
   - **Execution Interval**
   - **Language**
   - **OS Edition**

#. Click **Create**
#. Click **Apply** in top right corner

To Apply Newly Created Agent Action to Enforcement Policy
---------------------------------------------------------

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Find and click name of **desired Enforcement Policy**
#. Find **Agent Action** section and click Assign
#. Find **Agent Action** in the **Available** section and move to **Selected**
#. Click **Add**
#. Click **Update**
#. Click **Apply** in top right corner

To Remove and Delete Agent Action
---------------------------------

#. Go to **Policy** in the top panel
#. Go to **Enforcement Policy** in the left Policy panel
#. Find and click name of **desired Enforcement Policy**
#. Find **Agent Action** section and click **Assign**
#. Find **Agent Action** in the **Selected** section and move to **Available**
#. Click **Add**
#. Click **Update**
#. Go to **Policy > Enforcement Policy > Agent Action**
#. Find and click **Checkbox** of **desired Agent Action** to delete
#. Click **Tasks > Delete**
#. Click **Apply** in top right corner
