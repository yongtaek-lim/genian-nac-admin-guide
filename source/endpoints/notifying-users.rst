Notify User
===========

You can notify users with informational messages or warnings, and control how the message is 
presented using a slide-out notification, HTML, or redirect to a URL

#. Go to **Policy** in the top panel
#. Go to **Policy > Node Policy > Agent Action** in the left Policy panel
#. Find and click **Notify User** in the Agent Action window

Under **General** section

#. For **CWP Message**, add message to be displayed in accordance with the Policy
#. For **Label**, add labels to help categorize your plugins with custom labels that appear in the "Description" field

Under **Agent Actions** section

#. For **Boolean Operator**, choose **AND** or **OR** to add optional conditions
#. For **Settings**, click **Add** and select your optional conditions. **Criteria/Operator/Value**

Under **Plugin Settings** section

#. For **Contents for Slide-out Box Notification**, type in contents to display in slide-out box notification
#. For **CWP Page Redirection**, turn **On** to redirect to CWP page when a user clicks a slide-out notification

   - **CWP Page Redirection URL**, click **Use Template** or specify a URL for CWP redirection when a user clicks a slide-out notification

#. For **Enforcing Notification**, specify whether to disable to force closing a notification

   - **Notification Message Type**, specify a message type for a user notification (*Informational, Warning*)
   - **Generating Log for User Read Notification**, specify whether to generate a log when a user reads a notification

#. For **Execution Interval**, adjust Periodic Interval (*Seconds - months*) 
#. Enter in **CWP Message**, **Conditions**, and adjust **Agent Actions** based off of your network requirements
#. Click **Update**
#. Go to **Node Policy** in the left Policy panel
#. Click the **Default Policy** in Node Policy window
#. Find **Agent Action**. Click **Assign**
#. Find **Notify User** in the **Available** section. Select and drag it into the **Selected** section
#. Click **Add**
#. Click **Update**
