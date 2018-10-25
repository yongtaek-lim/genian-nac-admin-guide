Creating Enforcement Policy for Node Group
==========================================

**Enforcement Policies** work in a similar fashion to sorting in a mail room. All Nodes flow through a Priority List of **Enforcement Policies** to decide how much access they are allowed and which Groups they fit into. (*When creating custom Enforcement Policies, or re-arranging your Enforcement Policy list, two Enforcement Policies are required to stay where they are*)

- **Blocking Exceptions**: A custom Enforcement Policy cannot be placed above the Blocking Exceptions, or the Exceptions will not be properly applied
- **Default Policy**: A custom Enforcement Policy cannot be placed below the Default Policy,  as these are the bottom baselines for Enforcement

To Create An Enforcement Policy
-------------------------------

#. Go to **Policy** in the top panel
#. Go to **Policy > Enforcement Policy** in the left Policy panel
#. Click **Tasks > Create**
#. **Action** tab click **Next**
#. **General** tab create an **ID** and enter brief **Description** to identify what the Policy does (*Priority stays as default. Application mode should be Enable*) Click **Next**
#. **Node Group** tab select the **Node Group** that was created, move to **Selected** section and click **Next**
#. **Permission** tab select **Available Permission** and move to **Selected** and click **Next**
#. **Redirection** tab is **optiona**l to set **CWP** and **Switch Block options**. Click **Next**
#. **Agent Action** tab is **optional** to add **Agent Actions**
#. Click **Finish**
#. Find and click **Policy Checkbox**
#. Click **Tasks > Run Actions Now**
