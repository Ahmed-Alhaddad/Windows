
````md
# Basic Usage (PowerShell)

## Files and Directories

- `.` represents the **current directory**
- `..` represents the **parent directory**

---

## Get-ChildItem (`ls`)

Lists the contents of a directory.

```powershell
Get-ChildItem
````

---

## Set-Location (`cd`)

Changes the current working directory.

```powershell
Set-Location .\Documents\
```

---

## New-Item

Creates a new file or directory.

### Create an empty file

```powershell
New-Item file.txt
```

### Create a directory

```powershell
New-Item -ItemType Directory logs
```

For more examples:

```powershell
Get-Help New-Item -Examples
```

---

## Remove-Item (`rm`)

Deletes a file or directory.

```powershell
Remove-Item .\logs\
```

---

## Copy-Item (`cp`)

Copies files or directories.

```powershell
Copy-Item file.txt file1.txt
```

---

## Move-Item (`mv`)

Moves or renames files or directories.

### Move a file

```powershell
Move-Item .\file1.txt ..\Desktop\
```

### Move and rename a file

```powershell
Move-Item ..\Desktop\file1.txt .\file01.txt
```

---

## Get-Content (`cat`)

Displays the contents of a file.

```powershell
Get-Content .\file.txt
```

---

# System Processes (PowerShell)

## Get-Process

Displays a list of processes running on the system.

If used without parameters, it shows **all processes**.

```powershell
Get-Process
```

### Filter by name

```powershell
Get-Process -Name win*
```

---

## Stop-Process

Terminates a running process.
You can stop a process using its **ID** or **name**.

```powershell
Get-Process -Name explorer*
Stop-Process -Id 5432
```

⚠️ Be careful when stopping system or critical processes.

---

## Get-Service

Displays all services on the system along with their status.

```powershell
Get-Service
```

---

## Start-Service

Starts a service.

```powershell
Start-Service -Name Appinfo
```

---

## Stop-Service

Stops a service.

```powershell
Stop-Service -Name Appinfo
```

---

# Object Selection and Filtering

PowerShell uses **piping (`|`)** to send the output of one command to another.

This allows you to filter, select, and process data efficiently.

---

## Select-Object (`select`)

Selects specific properties from objects.

Example: show only process names and IDs.

```powershell
Get-Process | Select-Object ProcessName, Id
```

---

## Where-Object (`where`)

Filters objects based on conditions.

Example: show only running services.

```powershell
Get-Service | Where-Object Status -eq "Running"
```

### Common comparison operators

* `-eq` : Equals
* `-ne` : Not equal
* `-gt` : Greater than
* `-ge` : Greater than or equal
* `-lt` : Less than
* `-le` : Less than or equal

---

## Select-String

Searches for text patterns in files or strings.

Common uses:

* Searching text files
* Filtering output
* Pattern matching (regex supported)

### Search for a word in a file

```powershell
Select-String -Pattern "today" .\file.txt
```

Example output:

```
file.txt:1:The purpose of today's training is to defeat yesterday's understanding.
```

```

