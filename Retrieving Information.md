
````md
# Retrieving Information

## Retrieving System Information

### Get-ComputerInfo

Provides information about the operating system details, hardware information, and more.

```powershell
PS C:\Users\Administrator> Get-ComputerInfo
````

Example output:

```text
WindowsBuildLabEx               : 17763.1.amd64fre.rs5_release.180914-1434
WindowsCurrentVersion           : 6.3
WindowsEditionId                : ServerStandard
WindowsInstallationType         : Server
WindowsInstallDateFromRegistry  : 3/20/2024 4:48:20 AM
WindowsProductId                : 00429-00000-00001-AA815
WindowsProductName              : Windows Server 2019 Standard
WindowsRegisteredOwner          : Windows User
WindowsSystemRoot               : C:\Windows
WindowsVersion                  : 1809
BiosBIOSVersion                 : {BOCHS  - 1}
BiosCaption                     : Default System BIOS
...
```

---

## win32_OperatingSystem Class

Ideal for replicating the target system and conducting tests.

```powershell
PS C:\Users\Administrator> Get-WmiObject -Class win32_OperatingSystem
```

Example output:

```text
SystemDirectory : C:\Windows\system32
Organization    :
BuildNumber     : 17763
RegisteredUser  : Windows User
SerialNumber    : 00429-00000-00001-AA815
Version         : 10.0.17763
```

---

## Viewing Installed Updates

### Get-HotFix

Displays all updates (hotfixes) installed either via Windows Update or manually.

```powershell
PS C:\Users\Administrator> Get-HotFix
```

Example output:

```text
Source    Description  HotFixID    InstalledOn
------    -----------  --------    -----------
SRV2019  Update       KB4464455   10/29/2018
...
```

---

## Defender

Provides information about Windows Defender services.

```powershell
PS C:\Users\Administrator> Get-Service | Where-Object DisplayName -like '*Defender*'
```

Example output:

```text
Status   Name       DisplayName
------   ----       -----------
Running  mpssvc     Windows Defender Firewall
Stopped  Sense      Windows Defender Advanced Threat Protection
Running  WdNisSvc   Windows Defender Antivirus Network Inspection Service
Running  WinDefend  Windows Defender Antivirus Service
```

---

## Retrieving Information About Files

### Searching for Text in Files

Search for specific text across all files recursively.

```powershell
Get-ChildItem -Recurse *.* | Select-String -Pattern "SEARCH_STR"
```

---

### File Permissions

View the Access Control List (ACL) for a file or folder.

```powershell
Get-Acl file.txt
```

---

### File Hashes

Retrieve the hash of a file for verification or comparison.

```powershell
Get-FileHash file.txt
```
