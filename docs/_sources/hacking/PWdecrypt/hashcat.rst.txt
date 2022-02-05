Using Hashcat
****************

Cracking a Kerberos hash
##########################

`Go here to see where you get the output_file from <file:///usr/sysadmin/documentation/html/hacking/enum/AD/GetNPUsers.html>`_ .

Cracking a kerberos hash

.. code-block:: console

        hashcat -m 18200 <output_file> /usr/share/wordlists/rockyou.txt --force
