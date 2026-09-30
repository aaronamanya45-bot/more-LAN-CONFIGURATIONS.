# DHCP Commands

DHCP stands for Dynamic Host Configuration Protocol.

DHCP automatically provides network information such as:

* IP address
* Subnet mask
* Default gateway
* DNS server

## Windows DHCP Commands

Release an address:

```cmd
ipconfig /release
```

Renew an address:

```cmd
ipconfig /renew
```

View DHCP information:

```cmd
ipconfig /all
```

## Cisco DHCP Configuration

Enter configuration mode:

```text
enable
configure terminal
```

Create a DHCP pool:

```text
ip dhcp pool LAN
```

Set the network:

```text
network 192.168.1.0 255.255.255.0
```

Set the default gateway:

```text
default-router 192.168.1.1
```

Set DNS:

```text
dns-server 8.8.8.8
```

Exit:

```text
exit
```

## Exclude Addresses

Some addresses may be reserved for routers, servers or printers.

```text
ip dhcp excluded-address 192.168.1.1 192.168.1.20
```

## View DHCP Bindings

```text
show ip dhcp binding
```

## View DHCP Pool

```text
show ip dhcp pool
```

## Simple DHCP Example

```text
Router IP: 192.168.1.1

Network: 192.168.1.0/24

DHCP addresses:
192.168.1.21
192.168.1.22
192.168.1.23
...
```
