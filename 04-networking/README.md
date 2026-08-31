# 04 — Networking

This section covers basic Linux commands used to inspect network interfaces, IP addresses, routing information, network connectivity, active connections, and DNS information.

These commands are important for Linux system administration, network troubleshooting, and cybersecurity because they help provide visibility into how a system communicates with other devices and services.

## Commands Covered

### 1. `ip a` — Display Network Interfaces and IP Addresses

Displays information about the network interfaces on a Linux system, including their IP addresses and current state.

```bash
ip a
```

**Example:**

```bash
ip a
```

The output may show interfaces such as `lo`, `eth0`, or `wlan0`, along with their assigned IP addresses.

**Use case:**
Useful for identifying network interfaces and checking the IP addresses assigned to a system.

---

### 2. `ip link` — Display Network Interfaces

Displays information about network interfaces and their current status.

```bash
ip link
```

**Example:**

```bash
ip link
```

The output shows whether network interfaces are up or down.

**Use case:**
Useful for checking the status of network interfaces when troubleshooting connectivity problems.

---

### 3. `ip route` — Display the Routing Table

Displays the routing table used by the Linux system to determine where network traffic should be sent.

```bash
ip route
```

**Example:**

```bash
ip route
```

A typical routing table may contain a default route similar to:

```text
default via 192.168.1.1 dev eth0
```

This indicates that traffic destined for networks without a more specific route will be sent through the default gateway.

**Use case:**
Useful for troubleshooting routing and default gateway problems.

---

### 4. `ping` — Test Network Connectivity

Tests whether a destination can be reached over a network using ICMP Echo Requests.

```bash
ping destination
```

**Example:**

```bash
ping -c 4 8.8.8.8
```

The `-c 4` option sends four packets and then stops.

You can also test a domain name:

```bash
ping -c 4 google.com
```

**Use case:**
Useful for testing network connectivity and determining whether a host is reachable.

---

### 5. `ss` — Display Network Connections and Listening Ports

Displays information about network sockets, connections, and listening services.

```bash
ss
```

**Example:**

```bash
ss -tuln
```

The options mean:

* `-t` — TCP connections
* `-u` — UDP connections
* `-l` — Listening sockets
* `-n` — Display numerical addresses and ports

**Use case:**
Useful for identifying listening ports and network services running on a Linux system.

---

### 6. `traceroute` — Trace the Network Path

Shows the path that network packets take from your system to a destination.

```bash
traceroute destination
```

**Example:**

```bash
traceroute google.com
```

The command displays the network hops between your system and the destination.

**Use case:**
Useful for troubleshooting network paths and identifying where connectivity problems may occur.

---

### 7. `nslookup` — Query DNS Information

Queries the Domain Name System (DNS) to obtain information about a domain or hostname.

```bash
nslookup domain
```

**Example:**

```bash
nslookup google.com
```

The command can return information such as the IP address associated with a domain.

**Use case:**
Useful for troubleshooting DNS problems and investigating domain name resolution.

---

### 8. `dig` — Perform Detailed DNS Queries

Performs DNS queries and provides more detailed information than `nslookup`.

```bash
dig domain
```

**Example:**

```bash
dig google.com
```

You can also query a specific record type:

```bash
dig google.com MX
```

The `MX` record provides information about the mail servers associated with a domain.

**Use case:**
Useful for DNS troubleshooting and security investigations involving domains and DNS records.

---

### 9. `ip neigh` — View the Neighbor Table

Displays information about devices that the Linux system has recently communicated with on the local network.

```bash
ip neigh
```

**Example:**

```bash
ip neigh
```

The output can include IP addresses, MAC addresses, interfaces, and the state of neighboring devices.

**Use case:**
Useful for examining local network relationships and troubleshooting communication between devices.

---

### 10. `hostname` — Display the System Hostname

Displays the hostname assigned to the Linux system.

```bash
hostname
```

**Example:**

```bash
hostname
```

You can also use:

```bash
hostname -I
```

to display the IP addresses assigned to the system.

**Use case:**
Useful for identifying a system during network administration and security investigations.

---

## Understanding Basic Network Information

When working with Linux networking commands, several pieces of information are important:

```text
IP Address      → Identifies a device on a network
Default Gateway → Provides a path to other networks
DNS             → Translates domain names into IP addresses
Port            → Identifies a network service
Routing Table   → Determines where network traffic is sent
```

Understanding these concepts makes it easier to interpret the information provided by Linux networking commands.

---

## Practical Exercise

The following commands were used to inspect the network configuration and connectivity of the Linux system:

```bash
ip a
ip link
ip route
ping -c 4 8.8.8.8
ping -c 4 google.com
ss -tuln
nslookup google.com
dig google.com
ip neigh
hostname
```

This exercise demonstrates how to inspect network interfaces, identify IP addresses, examine routing information, test connectivity, inspect listening ports, perform DNS queries, and identify the local system.

## Cybersecurity Relevance

Networking commands are fundamental tools for cybersecurity professionals.

Security analysts may use them to:

* Identify a system's IP addresses and network interfaces.
* Investigate network connectivity.
* Examine routing information.
* Identify listening ports and network services.
* Investigate DNS activity.
* Examine devices communicating on a local network.
* Troubleshoot suspicious or unexpected network behavior.

For example, the `ss` command can help identify services listening for incoming connections, while `ip route` can help an analyst understand how a system communicates with other networks.

## Key Takeaway

Understanding Linux networking commands provides visibility into how a system connects to and communicates across a network. These skills form an important foundation for network troubleshooting, system administration, and cybersecurity analysis.

