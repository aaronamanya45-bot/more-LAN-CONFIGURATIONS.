# DNS Commands

DNS stands for Domain Name System.

DNS changes human-readable domain names into IP addresses.

For example:

```text
google.com
     ↓
IP address
```

## Windows

### `nslookup`

```cmd
nslookup google.com
```

### Clear DNS Cache

```cmd
ipconfig /flushdns
```

### Display DNS Configuration

```cmd
ipconfig /all
```

## Linux

### `nslookup`

```bash
nslookup google.com
```

### `dig`

```bash
dig google.com
```

### Short DNS Answer

```bash
dig google.com +short
```

### Check DNS Resolver

```bash
resolvectl status
```

## Test DNS

First test the IP address:

```bash
ping 8.8.8.8
```

Then test the domain:

```bash
ping google.com
```

If the IP works but the domain does not, there may be a DNS-related problem.

## Common DNS Servers

Examples include:

```text
Google DNS:
8.8.8.8
8.8.4.4

Cloudflare DNS:
1.1.1.1
1.0.0.1
```

These are examples of public DNS resolvers, not commands.
