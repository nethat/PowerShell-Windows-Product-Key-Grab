# PowerShell-Windows-Product-Key-Grab
PowerShell Module to grab windows Product Keys

From Powershell (start -> run -> powershell.exe)

>Set-ExecutionPolicy RemoteSigned

>Import-Module ./key.ps1

>Get-WindowsKey

By default will read local machine registry. If you want to search for keys that you've exported to another disk or USB, fire up regedit from the command line. Then click load hive, find the SOFTWARE hive that would normally be in:

C:\Windows\System32\config

Give the hive a name eg OLDPC

Then edit this line in key.ps1

From:

$regPath = "Software\Microsoft\Windows NT\CurrentVersion"

To:

$regPath = "OLDPC\Microsoft\Windows NT\CurrentVersion"

All credit to the original developer jakob@bindslet.dk. Have put it here on Github for my own personal access.

Tip to get Windows 8 key from BIOS

Boot to linux 
>ls /sys/firmware/acpi/tables

>sudo xxd /sys/firmware/acpi/tables/MSDM



