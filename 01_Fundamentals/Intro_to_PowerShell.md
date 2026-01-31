#To check the version of PowerShell.
```
PS C:\Users\user> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      5.1.19041.1237
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.19041.1237
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
```
--------------------------------------------
#Get-Process
 cmdlet is used to view processes, while #Get-Service
 cmdlet is used for information about services.
 --------------------------------------------
#Get-Help
command is used to get information about a command.

You can also use -? like: 
command -? 
to get help for the command
---------------------------------------------
#Get-Command
is a command used to list all commands, cmdlets, functions, 
filters, scripts, and even application commands that are installed in PowerShell.
The usage of this command detailed.
```
Get-Help -Name Get-Command -Detailed
```
----------------------------------------------
#Update-Help

If the help pages are missing or outdated, you can use the Update-Help
command to update them.

This command requires administrator privileges.
------------------------------------------------
Aliases

Aliases are special names in PowerShell that are used to create shortcuts for cmdlets,
functions, and scripts. They help you work faster by making commands shorter and easier to write.
For example, the alias cd
 can be used for the Set-Location
 cmdlet.

It is recommended to know aliases for faster PowerShell usage.
To view all aliases:
```
alias
```
To view the alias for a specific command, you can write the command after alias
:

```
alias cd
```
------------------------------------------------
