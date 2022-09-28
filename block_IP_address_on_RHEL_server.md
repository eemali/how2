# How to block IP address on RHEL server

## Introduction

If you wish to block an IP address from accessing your server for some reason, you can do this by changing the `iptables` rules. Follow the steps given below to perform this task successfully.

### Step 1: Login as `root` user

### Step 2: Add new `iptables` rule

Enter the following rule to block an IP address from accessing your server

```bash
iptables -A INPUT -s IP-ADDRESS -j DROP
```

Replace `IP-ADDRESS` with the actual IP address that you want to block completely. The above rule will drop all packets coming from that particular IP to all server ports.

### Alternate option – Block access to a specific port

To block server access from an IP address only on a specific port on the server, the following syntax must be used

```bash
iptables -A INPUT -s IP-ADDRESS -p tcp --destination-port port_number -j DROP
```

Replace the `port_number` with the actual one that you want to block access to.

## Saving `iptables` rule

Save your `iptables` rules with this command:

```bash
service iptables save
```

## To revoke the drop rule

To revert the rule and to allow the IP address to access the server run the following command

### For all ports:

```bash
iptables -D INPUT -s IP-ADDRESS -j DROP
```

### For specific port:

```bash
iptables -D INPUT -s IP-ADDRESS -p tcp --destination-port port_number -j DROP
```

Then save the changes using the commands mentioned previously.
