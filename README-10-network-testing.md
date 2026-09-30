# Network Testing Commands

Network testing helps determine whether devices can communicate successfully.

## 1. Ping

```bash
ping 8.8.8.8
```

Tests basic connectivity.

## 2. Ping the Localhost

```bash
ping 127.0.0.1
```

This tests the local TCP/IP stack.

## 3. Ping the Gateway

Example:

```bash
ping 192.168.1.1
```

This checks communication with the local router.

## 4. Traceroute

Linux:

```bash
traceroute google.com
```

Windows:

```cmd
tracert google.com
```

Shows the path taken by packets.

## 5. Pathping

Windows:

```cmd
pathping google.com
```

Provides information about packet loss and network paths.

## 6. NSLookup

```cmd
nslookup google.com
```

Tests DNS resolution.

## 7. Netstat

```cmd
netstat -ano
```

Shows active connections and listening ports.

Linux:

```bash
ss -tuln
```

## 8. Test a Port

PowerShell:

```powershell
Test-NetConnection google.com -Port 443
```

## Testing Sequence

A useful sequence is:

```text
1. Check cable/Wi-Fi
       ↓
2. Check IP address
       ↓
3. Ping localhost
       ↓
4. Ping gateway
       ↓
5. Ping an external IP
       ↓
6. Test DNS
       ↓
7. Trace the route
```
