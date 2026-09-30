# VLAN Commands

VLAN stands for Virtual Local Area Network.

VLANs can be used to divide a physical network into logical networks.

## Create a VLAN

```text
enable
configure terminal

vlan 10
name STUDENTS
exit
```

## Create Another VLAN

```text
vlan 20
name STAFF
exit
```

## Configure an Access Port

```text
interface gigabitEthernet 0/1
switchport mode access
switchport access vlan 10
```

## Configure a Trunk Port

```text
interface gigabitEthernet 0/24
switchport mode trunk
```

## Display VLANs

```text
show vlan brief
```

## Display Interfaces

```text
show interfaces status
```

## Display Trunk Information

```text
show interfaces trunk
```

## Remove a VLAN

```text
no vlan 10
```

## Example

Suppose a school has:

```text
VLAN 10 = Students
VLAN 20 = Staff
VLAN 30 = Administration
```

The VLAN configuration separates these groups logically even if they use the same physical switch.

## Important

Devices in different VLANs normally need routing between VLANs if they are required to communicate.
