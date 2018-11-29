The blocked Nodes can't redirect to CWP page
============================================

+------------------------------------------+
|Term Definition                           | 
+==========================================+
|CWP – Captive Web Portal                  |
+------------------------------------------+
|HSTS – HTTP Strict Transport security     |
+------------------------------------------+
|HPKP – HTTP Public Key Pinning            |
+------------------------------------------+
|MITM – Man In The Middle                  |
+------------------------------------------+

You are not connected to the CWP page from the PC being controlled by GNAC
Sometimes you see only the phrase "Your connection is not private." on the browser.

This is a problem that occurs when a user who does not comply with the security policy is using an HTTPS service to connect to a specific site. 
GNAC basically uses the MITM method to display the CWP screen to the target user However, the browser functions called HSTS and HPKP (Verification of certificates in the browser) do not show the CWP page.
so, let's examine whether this problem will occur in the following order.

#. How GNAC show the CWP page to the controlled PC with HTTP communication
#. How GNAC shows the CWP page to the controlled PC that is trying to HTTPS communication

- HTTPS communication method
- HTTPS control method in GNAC

3. The reason why the message "Your connection is not private" appears on the browser screen when a user PC that does not comply with security policy accesses a specific website
- Explanation of HSTS and HPKP
- Reason for not showing CWP page

1. How GNAC show the CWP page to the controlled PC with HTTP communication
--------------------------------------------------------------------------

GNAC will show you what security policies you need to comply with through CWP when your PC attempts to surf through a browser that does not meet the security policy rules in your company.

In order to show the captive web portal to users who do not satisfy the policy, GNAC monitors the process of network communication by the user PC, and when the user PC requests the web screen of the server to which the user wants to access, GNAC provides the CWP page to Redirect so that your PC will see the CWP page of GNAC instead of the page you requested.

But you may have one question
In the case of HTTP, GNAC can check all communication flow based on the plaintext
In the case of HTTPS, It is questionable how GNAC can check packets that a non-compliant user PC requests a web screen to the server.

First of all, it is necessary to understand the communication method of HTTPS in order to know about this part.

2. How GNAC shows the CWP page to the controlled PC that is trying to HTTPS communication
-----------------------------------------------------------------------------------------

A. HTTPS communication method
+++++++++++++++++++++++++++++

Basically, the problem occurs only when the PC is connected to a specific URL that provides HTTPS service. First, I will inform you about general communication method of HTTPS.

**The communication connection method of HTTPS is as follows.**
 

.. image:: /images/communication-https.jpg
   :width: 700px

HTTPS communication also requires intercommunication between the Web Server and the PC for encrypted communication before creating a cryptographic session.

#. Client hello: PC notifies Web Server to HTTPS communication
#. Server Hello, Certificate: The server passes the certificate to the client, the client determines that the certificate is a trusted certificate
#. Client Key Exchange: The client sends the pre-master-secret key to the Web Server, Symmetric key sharing
#. Finish: After the end of the negotiation process, communication is exchanged by a symmetric key exchange

After that, encrypted communication is performed between PC and Web Server
Packets that request Web screens from the PC to the Web Server are also transmitted using the encrypted channel.

B. HTTPS control method in GNAC
+++++++++++++++++++++++++++++++

Now GNAC will show you how to show CWP pages on your PC with HTTPS communication.

**This method uses MITM attacks**

PCs that do not comply with the security policy are in a state where the ARP table is modulated. All communication is done through the network sensor. When communicating with the Web Server, the Network Sensor communicates instead of Web Server pretending.

.. image:: /images/mitm-attack.jpg
   :width: 600px
 
The important point here is that the server certificate is transmitted to the CA certificate (FAKE Certificate) created by GNAC so that the encrypted communication is not connected to the Web Server but the session is established with GNAC so that the communication contents can be checked on the network sensor. 
So, GNAC is able to show the CWP screen on a PC that does not comply with the security policy
If you follow the above method, it seems that you can show the CWP screen on the PC that connects to all Web Servers running HTTPS service.
However, I will tell you why users who do not comply with the security policy can only see the message "Your connection is not private" on the browser screen when accessing a specific website and cannot see the CWP screen.

3. The reason why the message "Your connection is not private" appears on the browser screen when a user PC that does not comply with security policy accesses a specific website
This part is caused by HSTS and HPKP function. Let's first examine the functions of HSTS and HPKP.

A. Explanation of HSTS and HPKP
+++++++++++++++++++++++++++++++

- **HSTS(HTTP Strict Transport security)**

What is HSTS?

When the user tries to connect to the HTTPS server through HTTP
The server sends 'Strict-Transport-Security' contents to the user's PC in its header field that the browser can only access to the browser through HTTPS
The user browser that receives the message tells the PC to use HTTPS instead of HTTP when connecting to Web Server.

- **HPKP(HTTP Public Key Pinning)**

What is HPKP?

Certain site's certificate PIN values are pre-stored in the browser
Comparing the PIN value of certificate transmitted from Web server to PC when attempting HTTPS communication
If the PIN value stored in the browser is different from the PIN value of the certificate transmitted from the Web server, it is recognized as an invalid certificate.
If it is an invalid certificate, it controls communication and prevents man in the middle attack.

B. Reason for not showing CWP page
++++++++++++++++++++++++++++++++++

I will now explain why GNAC cannot show CWP pages while controlling non-compliant users. 

When the control target PC accesses a specific site that performs HTTPS communication, GNAC delivers the GNAC certificate to the control target PC instead of the specific site certificate. 

Here, the browser has a unique PIN value of a specific site (Google, Paypal, Twitter, etc.) certificate with HPKP function, and compares the PIN value of the certificate received from GNAC with the PIN value of the specific site pre-registered in the browser.
If the PIN value of the specific site is compared with the PIN value of the GNAC certificate and it is judged to be different, the GNAC cannot show the CWP page on the user PC because an encryption session cannot be established between the control target PC and the GNAC..

This is why the control target user PC is not redirected to the CWP screen when accessing a specific site and only the message "Your connection is not private" is displayed.

This is a problem with all security devices that use the redirection feature and we are currently considering other countermeasures.

.. code:: bash

   How to verify information on a site with restricted certificates
   Chrome: Enter URL via Chrome browser - chrome://net-internals/#hsts
