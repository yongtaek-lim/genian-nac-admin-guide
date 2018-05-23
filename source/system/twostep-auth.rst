2-Step Authentication
=====================

Genian NAC uses 2-Step Authentication with OTP Google Authenticator to add a second level of
authentication to an account log-in. Once Google Authenticator is installed a QR Code will
display so you can scan it with your smartphone or tablet. A six digit code will then be
presented to then enter as the final step in your 2-Step Authentication.
(*Google Authenticator six-digit code is continuously changing so enter it in quickly*)

To Enable 2-Step Authentication For Administrator Account
---------------------------------------------------------

#. Go to Management > User in the top panel
#. Go toAdministrators in the left User Management panel
#. Find and click Username of Administrator account in the main Administrators window
#. Find and click Administrator tab
#. Find General: 2-Step Authentication section in the main window
#. Click OTP (Google Authenticator) in drop-down
#. Find Notification Options section. Enter the following:
#. Mobile Phone (*e.g. 123-456-7890*)
#. Display Phone Number (*This is an optional number you want visible to sender*)
#. Email (*Multiple Email Addresses separated by commas*)
#. Click Update

To Enable 2-Step Authentication For The Policy Server
-----------------------------------------------------

#. Go to Preferences in the top panel
#. Go to General > Console in the left Preferences panel
#. Find Web Console: 2-Step Verification Methods section in the main Console window
#. Click Checkbox for OTP (Google Authenticator)
#. Click Update

To Setup Google Authenticator
-----------------------------

#. On your Mobile Phone go to App Store to download Google Authenticator
#. Logout from Policy Server UI and Login again
#. 2-Step Authentication wizard appears to setup Google Authenticator
#. Click Start
#. Select Mobile Phone type, Android or iPhone
#. Select Application Method to Install via QR Code (*QR Code will appear as an example*)
#. Click OK then Next (*Make sure you have Google Authenticator installed on Mobile Phone and ready to scan QR Code*)
#. Select QR Code in drop-down and then click Generate Security Key
#. Using Mobile Phone scan the QR Code that was just generated
#. Mobile Phone will present a 6 digit code that you will need to remember and quickly enter it into the Google Authenticator Wizard
#. Click OK
