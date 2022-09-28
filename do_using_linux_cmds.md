# Frequently used LINUX Commands

### 1. Check status of firewall

```bash
service firewalld status
```

### 2. Stop firewall

```bash
service firewalld stop
```

### 3. Diable firewall

```bash
systemctl disable firewalld.service
```

### 4. Add entry in route table

```bash
ip route add 224.0.0.0/4 dev eth0 
```

> Note: Replace `eth0` with name of etherent interface on your Linux system. 