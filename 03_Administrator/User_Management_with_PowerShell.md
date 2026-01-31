````md
# User Management with PowerShell

PowerShell is a powerful tool for managing users and groups in Windows and Active Directory (AD). It allows administrators to create and delete user accounts, reset passwords, manage group memberships, and more.

---

## Overview of Active Directory

Active Directory (AD) is a Microsoft directory service used in Windows Server environments. It provides a centralized database for managing:

- Users
- Computers
- Groups
- Printers
- Applications
- Network resources

With AD, administrators can:
- Create, modify, and delete user accounts
- Reset passwords and enforce password policies
- Manage permissions using security groups
- Apply Group Policies for consistent configuration

Active Directory scales from small networks to large enterprise environments.

---

## RSAT (Remote Server Administration Tools)

RSAT allows you to manage Windows Servers and Active Directory remotely from a Windows client.

RSAT includes:
- GUI management tools
- PowerShell modules with AD and server-related cmdlets

### RSAT Installation

1. Open **Start Menu**
2. Go to **Settings**
3. Select **Apps**
4. Click **Optional features**
5. Choose **Add a feature**
6. Search for **RSAT**
7. Select and install it

> PowerShell commands require **administrator privileges**.

---

## Local User Management

### List Local Users
```powershell
Get-LocalUser
````

### Create a Local User

```powershell
New-LocalUser -Name "j.doe" -Password (ConvertTo-SecureString "password123" -AsPlainText -Force)
```

### Modify a Local User

```powershell
Set-LocalUser -Name "j.doe" -Description "Test user"
```

### Disable / Enable a Local User

```powershell
Disable-LocalUser -Name "j.doe"
Enable-LocalUser -Name "j.doe"
```

### Delete a Local User

```powershell
Remove-LocalUser -Name "j.doe"
```

---

## Local Group Management

### List Local Groups

```powershell
Get-LocalGroup
```

### Create a Local Group

```powershell
New-LocalGroup -Name "Students"
```

### Modify a Local Group

```powershell
Set-LocalGroup -Name "Students" -Description "Training group"
```

### Add / Remove Group Members

```powershell
Add-LocalGroupMember -Group "Students" -Member "j.doe"
Remove-LocalGroupMember -Group "Students" -Member "j.doe"
```

### Delete a Local Group

```powershell
Remove-LocalGroup -Name "Students"
```

---

## Active Directory Users

### List All AD Users

```powershell
Get-ADUser -Filter *
```

### Get a Specific AD User

```powershell
Get-ADUser "j.doe"
```

### Create an AD User

```powershell
New-ADUser -Name "j.doe" -SamAccountName j.doe -AccountPassword (ConvertTo-SecureString "sifre123!" -AsPlainText -Force)
```

### Modify an AD User

```powershell
Set-ADUser -Identity "j.doe" -Surname "Doe"
```

### Delete an AD User

```powershell
Remove-ADUser "j.doe"
```

---

## Active Directory Groups

### List All AD Groups

```powershell
Get-ADGroup -Filter *
```

### Create an AD Group

```powershell
New-ADGroup -Name "Students" -GroupScope Universal
```

### Modify an AD Group

```powershell
Set-ADGroup -Identity "Students" -Description "Learning group"
```

### View Group Members

```powershell
Get-ADGroupMember "Students"
```

### Add / Remove Group Members

```powershell
Add-ADGroupMember -Identity "Students" -Members j.doe
Remove-ADGroupMember -Identity "Students" -Member j.doe
```

### Delete an AD Group

```powershell
Remove-ADGroup "Students"
```

---


