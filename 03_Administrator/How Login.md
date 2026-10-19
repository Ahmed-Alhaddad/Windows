How to View Logged-On Users in Windows

Learn how to view logged-on users in Windows using CMD and PowerShell.

1. Using CMD (Command Prompt)

Display logged-on users

query user

Alternative command:

quser

Show only active sessions

query user | findstr "Active"

Display local Windows user accounts

net user

Display details about a specific local user

net user <username>

Note: net user lists local accounts by default. It does not show which accounts are currently logged on.

2. Using PowerShell

Display the currently logged-on user on the local computer

Get-CimInstance Win32_ComputerSystem |
    Select-Object -ExpandProperty UserName

Display logged-on sessions

quser

Show only active sessions

quser | Select-String "Active"

Note: quser and query user are Windows session-management commands that can also be run from PowerShell.