NMAP cheatsheat
*****************

TCP scan all ports

.. code-block:: console

	nmap -sC -sV -p- <IP>

UDP scan all ports

.. code-block:: console

	nmap -sU -sV -p- <IP>

smb enumeration

.. code-block:: console

	nmap --script smb-vuln* -p 137,139,445 <IP>  
