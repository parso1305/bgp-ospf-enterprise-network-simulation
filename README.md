

## Problem
Large scale networks are divided into **Autonomous Systems (AS)** to maintain scalable routing and better network management.

Inside an organization, routers must exchange routing information dynamically, while communication between different networks must be handled by an exterior routing protocol.

The goal of this project is to simulate:

- Internal routing inside an organization
- Communication between multiple autonomous systems
- End-to-end connectivity between hosts in different networks

---

## Solution
This network simulation uses a **multi-layer routing architecture**.

- **OSPF (Open Shortest Path First)** is used for routing inside each autonomous system.
- **BGP (Border Gateway Protocol)** is used for routing between autonomous systems.
- **DHCP** is used to automatically assign IP addresses to client devices.
- **Static and default routes** assist in directing traffic to external networks.

The topology represents how enterprise networks connect with other organizations or service providers.

---

## Features
- Dynamic routing using **OSPF**
- Inter-AS routing using **BGP**
- DHCP configuration for automatic IP assignment
- Multi-router enterprise topology
- End-to-end connectivity testing
- Cisco Packet Tracer based simulation

---

## Architecture / How It Works
The topology is divided into several sections:

### Local Network
- Multiple PCs connected to switches
- DHCP router assigns IP addresses
- Access routers connect LAN networks to the routing backbone

### Autonomous System 100
- Internal routers connected using OSPF
- Dynamic route exchange inside the AS

### Autonomous System 200
- Separate routing domain with its own internal routing

### Inter-AS Connectivity
- Border routers establish BGP sessions
- Routes are exchanged between the two autonomous systems

This allows hosts from one network to communicate with servers located in another autonomous system.

---

## Installation

1. Install **Cisco Packet Tracer**
2. Clone the repository

```bash
git clone https://github.com/yourusername/autonomous-system-network.git
```

3. Open the `.pkt` file using Cisco Packet Tracer.

---

## Usage

Open the Packet Tracer project and run the simulation.

Useful verification commands inside router CLI:

```bash
show ip route
show ip ospf neighbor
show ip bgp summary
show running-config
```

Connectivity between networks can be verified using:

```bash
ping <destination-ip>
```

## Future Improvements

- Implement route redistribution between OSPF and BGP
- Add redundancy using multiple border routers
- Introduce ACL based network security
- Simulate network failures and routing convergence

---

## Author

**Parth Soni**

Cisco Packet Tracer Networking Project
