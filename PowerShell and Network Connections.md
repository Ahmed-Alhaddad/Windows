````md
# PowerShell and Network Connections

PowerShell is a powerful tool for viewing and managing network settings. It allows administrators and users to check IP addresses, test connections, and interact with network resources.

---

## Gathering Network Information

### Get-NetIPAddress
The `Get-NetIPAddress` cmdlet retrieves IP address information and other IP configuration details for network interfaces.

```powershell
Get-NetIPAddress
````

---

## Legacy Network Commands (CMD)

These commands are older but still widely used and supported in PowerShell.

### IPConfig

Displays network configuration details such as IP address, subnet mask, and default gateway.

```powershell
ipconfig
```

---

### Netstat

Displays active TCP/IP connections, listening ports, and connection states.

```powershell
netstat
```

---

### Nslookup

Queries DNS to resolve domain names to IP addresses.

```powershell
nslookup example.com
```

---

### ARP

Shows the ARP cache, which maps IP addresses to MAC addresses on the local network.

```powershell
arp -a
```

---

## Testing Network Connections

### Test-NetConnection

Tests network connectivity to a remote host or service.

```powershell
Test-NetConnection
```

---

## Downloading Files

### Invoke-WebRequest

Used to send web requests and download files from the internet.

```powershell
Invoke-WebRequest -Uri "https://example.com/file.png" -OutFile "file.png"
```

* **-Uri**: Specifies the web address
* **-OutFile**: Specifies the output file name

---


