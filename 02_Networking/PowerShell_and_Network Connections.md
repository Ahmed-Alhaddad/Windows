````md
# PowerShell and Network Connections

This guide introduces basic PowerShell and Windows networking commands used to view, test, and troubleshoot network connections.

---

## 📡 Gathering Network Information

### Get-NetIPAddress
Retrieves IP address and configuration details for all network interfaces.

#powershell
```
Get-NetIPAddress
```
````
---

## 🧰 Legacy Network Commands (CMD)

These commands are older but still commonly used and fully supported in PowerShell.

### IPConfig

Displays IP configuration details such as:

* IP address
* Subnet mask
* Default gateway

```powershell
ipconfig
```

---

### Netstat

Shows active TCP/IP connections, listening ports, and connection states.

```powershell
netstat
```

---

### Nslookup

Queries DNS to resolve domain names to IP addresses.

```powershell
nslookup example.com
```

Useful for DNS troubleshooting.

---

### ARP

Displays the ARP cache, mapping IP addresses to MAC addresses on the local network.

```powershell
arp -a
```

---

## 🔌 Testing Network Connections

### Test-NetConnection

Tests network connectivity to a remote host or service.

```powershell
Test-NetConnection
```

---

## ⬇️ Downloading Files

### Invoke-WebRequest

Used to download files or interact with web services.

```powershell
Invoke-WebRequest -Uri "https://example.com/file.png" -OutFile "file.png"
```

**Parameters:**

* `-Uri` — Web address of the resource
* `-OutFile` — Name of the downloaded file

#tnc
Tnc IP address:port

#udl file
create notepad like file.udl to check the database
open notepad as administrator
and then save it as name.udl 
open the file start chack your database
---

## 📘 Notes

* All commands can be run directly in **PowerShell**
* Administrative privileges may be required for some commands

---

