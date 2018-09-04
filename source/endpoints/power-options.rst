Controlling Power Options
=========================
 
You can control the power options (e.g. Sleep, Restart, and Shutdown) and control how long the 
Windows device stays up and running after it wakes from sleep

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Click the **desired Policy ID** in Node Policy window
#. Find and click **Control Power Options** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Power Control Action**, sepcify how to control the power of the device (*Sleep, Restart, Shutdown*)
#. For **Power Control Action**, turn **On** to enforce the power control
#. For **Delay Threshold**, adjust the time to delay applying the policy (*Seconds - hours*)
#. For **Runtime Remaining Threshold**, adjust the runtime remaining before an action is performed (*Seconds - hours*)
#. For **Uptime for Power Control**, adjust the time to control power after wake (*minutes - months*)
#. For **Displaying Header**, turn **On** to display a header of the dialog box
#. For **Method for Displaying Message**, specify how to display the message below (*HTML, Image*)
#. For **Message Contents**, specify the message contents, text and height
#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*)
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Control Power Options** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
