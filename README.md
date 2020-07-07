# ActiveDirectoryLostClientLocator
Summary: Finds computers in Active Directory that do not have a manager or description listed. Returns information about lost computers in CSV format.

This PowerShell script iterates through computers whose <strong>ManagedBy</strong> and <strong>Description</strong> attributes are <strong>null</strong>. Based on this list, the script pings each computer and returns the results into a CSV file which is exported to the scripts root, with the date as the title. Result columns include:

-Computer (Hostname)
<br>-Status (Shows Offline or Online depending on ping results)
<br>-LastLogon (Last date that computer was logged onto)
<br>-IPv4 (IPv4 Address)
<br>-OS (Operating System)

The results are sorted by Status, then LastLogon.
