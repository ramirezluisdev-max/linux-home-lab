# DNS Troubleshooting Guide

## Overview

This guide documents the process used to diagnose and troubleshoot DNS-related issues in my Linux home lab.

---

# What is DNS?

DNS (Domain Name System) translates human-readable domain names into IP addresses.

Example:

```
google.com
↓

142.250.xxx.xxx
```

Without DNS, websites cannot be reached using their names.

---

# Symptoms of DNS Problems

- Websites do not load
- Pinging an IP address works
- Pinging a hostname fails
- "Temporary failure in name resolution"
- Package downloads fail

---

# Commands Used

## View DNS servers

```bash
cat /etc/resolv.conf
```

---

## Test DNS

```bash
ping google.com
```

---

## Test Internet without DNS

```bash
ping 8.8.8.8
```

If this works but google.com does not, DNS is likely the problem.

---

## Display interface configuration

```bash
nmcli dev show wlan0
```

---

# Troubleshooting Process

1. Verified network connection.
2. Confirmed valid IP address.
3. Verified default gateway.
4. Examined DNS configuration.
5. Compared hostname resolution with direct IP connectivity.
6. Reviewed NetworkManager configuration.
7. Reviewed system logs.

---

# Lessons Learned

During troubleshooting I learned:

- Internet connectivity and DNS are separate issues.
- A system can have Internet access while still failing DNS lookups.
- NetworkManager supplies DNS information to the system.
- DNS should always be checked before assuming Internet connectivity has failed.

---

# Skills Demonstrated

- Linux Administration
- DNS
- Network Troubleshooting
- NetworkManager
- Linux Command Line
- Problem Solving
