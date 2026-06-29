# Linux Networking Commands Reference

## Overview

This document contains Linux networking commands I have learned while building my home lab. It serves as both a study guide and a quick reference for diagnosing and troubleshooting network issues.

---

# Interface Information

## Show all network interfaces

```bash
ip addr
```

Displays all network interfaces, IP addresses, and interface status.

---

## Show routing table

```bash
ip route
```

Displays the routing table and default gateway.

---

## Show active NetworkManager connections

```bash
nmcli connection show --active
```

Lists active network connections.

---

## Show device details

```bash
nmcli dev show wlan0
```

Displays detailed information about the wireless adapter.

---

# Wireless Commands

## Check Wi-Fi power saving

```bash
iw dev wlan0 get power_save
```

Shows whether wireless power saving is enabled.

---

## Disable Wi-Fi power saving

```bash
iw dev wlan0 set power_save off
```

Disables power saving to improve connection stability.

---

# Connectivity Testing

## Ping the default gateway

```bash
ping 192.168.4.1
```

Verifies communication with the router.

---

## Ping Google

```bash
ping google.com
```

Tests Internet connectivity and DNS resolution.

---

## Ping a public DNS server

```bash
ping 8.8.8.8
```

Tests Internet connectivity without relying on DNS.

---

# DNS

## View DNS configuration

```bash
cat /etc/resolv.conf
```

Displays configured DNS servers.

---

# System Logs

## View system journal

```bash
journalctl
```

Displays system logs.

---

## Follow live logs

```bash
journalctl -f
```

Shows log messages in real time.

---

# Package Management

## Update package lists

```bash
sudo apt update
```

Refreshes available package information.

---

## Upgrade installed packages

```bash
sudo apt upgrade
```

Installs available package updates.

---

# Lessons Learned

Throughout this home lab I have used these commands to troubleshoot:

- Wi-Fi connectivity
- DNS failures
- DHCP configuration
- Routing issues
- NetworkManager configuration
- Driver troubleshooting
- Linux system diagnostics

This command reference will continue to grow as additional troubleshooting scenarios are completed.
