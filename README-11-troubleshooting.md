# Network Troubleshooting Commands

Network troubleshooting is the process of finding and fixing problems that prevent devices from communicating.

## Step 1: Check the IP Address

Windows:

```cmd
ipconfig
```

Linux:

```bash
ip addr
```

Check whether the device has a valid IP address.

## Step 2: Test the Local TCP/IP Stack

```bash
ping 127.0.0.1
```

If this fails, there may be a problem with the local network configuration.

## Step 3: Test the Default Gateway

Example:

```bash
ping 192.168.1.1
```

If this fails, check the connection between the computer and the local router.

## Step 4: Test Internet Connectivity

```bash
ping 8.8.8.8
```

If the gateway works but this does not, investigate the wider network or Internet connection.

## Step 5: Test DNS

```bash
nslookup google.com
```

You can also try:

```bash
ping google.com
```

## Step 6: Trace the Route

Windows:

```cmd
tracert google.com
```

Linux:

```bash
traceroute google.com
```

## Step 7: Check the Routing Table

Windows:

```cmd
route print
```

Linux:

```bash
ip route
```

Cisco:

```text
show ip route
```

## Step 8: Check Network Interfaces

Linux:

```bash
ip link
```

Cisco:

```text
show ip interface brief
```

## Step 9: Check Active Connections

Windows:

```cmd
netstat -ano
```

Linux:

```bash
ss -tuln
```

## Common Problems

### Problem: No IP Address

Try:

```cmd
ipconfig /renew
```

### Problem: DNS Not Working

Try:

```cmd
ipconfig /flushdns
```

Then test:

```cmd
nslookup google.com
```

### Problem: Cannot Reach Gateway

Check:

* Ethernet cable
* Wi-Fi connection
* IP address
* Subnet mask
* Default gateway
* Router connection

### Problem: One Website Does Not Work

Test another website.

For example:

```bash
ping google.com
```

If other sites work, the problem may be specific to that website or service.

## Troubleshooting Principle

Do not change many settings at once.

Test one part of the network at a time and identify where communication stops.

```text
Computer
   ↓
Network Interface
   ↓
Local Network
   ↓
Default Gateway
   ↓
Internet
   ↓
DNS
   ↓
Destination
```
