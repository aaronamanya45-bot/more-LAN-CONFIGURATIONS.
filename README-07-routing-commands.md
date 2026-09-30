# Routing Commands

Routing determines how network packets move from one network to another.

## View Routing Table

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

## Static Route on Cisco

```text
ip route 192.168.2.0 255.255.255.0 192.168.1.2
```

This tells the router how to reach:

```text
192.168.2.0/24
```

through:

```text
192.168.1.2
```

## Default Route

```text
ip route 0.0.0.0 0.0.0.0 192.168.1.1
```

## Display Routes

Cisco:

```text
show ip route
```

Linux:

```bash
ip route show
```

Windows:

```cmd
route print
```

## Delete a Route on Linux

```bash
sudo ip route del 192.168.2.0/24
```

## Add a Route on Linux

```bash
sudo ip route add 192.168.2.0/24 via 192.168.1.1
```

## Routing Protocol Examples

Common routing protocols include:

* RIP
* OSPF
* EIGRP
* BGP

## Basic OSPF Example

Cisco:

```text
router ospf 1
network 192.168.1.0 0.0.0.255 area 0
```

## Important

Routing commands must be used carefully because incorrect routes can prevent devices from communicating.
