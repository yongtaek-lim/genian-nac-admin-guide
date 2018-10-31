Reporting unsupported hardware
==============================

If you have unsupported hardware, such as storage devices, Ethernet adapters, or wireless LAN adapters, during the Genian NAC installation
process, please collect the information through the following procedure and send it to us at help@genians.com.

#. Install generic Linux distribution like Ubuntu_

#. Open Terminal

#. Type following command to create report.txt

    .. code-block:: shell

        $ sudo apt install pciutils lshw
        $ dmesg > report.txt
        $ lspci >> report.txt
        $ lshw >> report.txt

#. Send us a report.txt file

.. _Ubuntu: https://www.ubuntu.com/
