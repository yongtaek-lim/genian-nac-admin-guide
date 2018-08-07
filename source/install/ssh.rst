Allow SSH Access
================

Genian NAC by default does not allow for SSH access to the appliance until the Administrator allows for this access by adding a 
single IP Address or a Network Address. You can add a single IP Address if you are the only Administrator, or add Network address 
if you many Administrators. (*e.g. 192.168.10.10, 192.168.10.0/24, or any IP using 0.0.0.0/0*)

Allow IP Source for SSH Access
------------------------------

#. Login to your On-Prem device  https://<IP Address>/mc
#. Go to **System** in the top panel
#. Find and click on the **IP Address**
#. Select the **Appliance** tab
#. Find Security section  and add in your **IP Network** into the **Approved SSH Source IP** 1 field
#. Click **Update**
#. Re-open your **Putty** session and attempt to connect again

