Configuring Password Policy
===========================

To configure Password Policy that is enforced onto your end users

Configure Password Policy
-------------------------

#. Go to **Preferences** in the top panel
#. Go to **User Authentication > User Account** in the left Preferences panel
#. Enter the following options:

   - **Encryption Type** - Either HMAC-SHA256 or Windows NT-Hash (*Note: You should select NT-Hash for MSCHAPv2 Authentication by RADIUS Server*)
   - **Minimum Length** - Must be at least 9 Characters
   - **Maximum Length** - Is 30 characters
   - **Start with Alphabet** - To force password to start with a letter
   - **Uppercase/Lowercase** - To force a mixture of Uppercase and Lowercase letters
   - **Repeated Characters** - To specify whether or not they are allowed to have repeated characters in a row. i.e. “000, aaa”
   - **Numerical or Alphabetical Order** - To allow or not allow a numerical or alphabetical order
   - **Regular Expression** - To use to validate a password. Enter in Expression and Error message
   - **Username Password Restriction** - Passwords will not be able to use usernames
   - **Password Blacklist** - Block weak or easily guessed passwords. This will require you to upload a Blacklist file

#. Click **Update**
