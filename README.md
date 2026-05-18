# Secure Enterprise Multi-Router OSPF Lab

## Project Overview

This project demonstrates a secure enterprise network using OSPF dynamic routing with MD5 authentication between routers.

The topology includes:
- 3 Cisco routers
- 3 switches
- 6 PCs
- Redundant routing paths
- Secure OSPF neighbor authentication

---

# 🖧 Network Topology

text
              R3
             /  \
            /    \
          R1------R2


---

# IP Addressing Plan

| Device | Interface | IP Address |
|---|---|---|
| R1 | g0/0 | 192.168.10.1/24 |
| R1 | g0/1 | 10.0.13.1/30 |
| R1 | g0/2 | 10.0.12.1/30 |
| R2 | g0/0 | 192.168.20.1/24 |
| R2 | g0/1 | 10.0.23.1/30 |
| R2 | g0/2 | 10.0.12.2/30 |
| R3 | g0/0 | 192.168.30.1/24 |
| R3 | g0/1 | 10.0.13.2/30 |
| R3 | g0/2 | 10.0.23.2/30 |

---

# OSPF Security

MD5 authentication is configured between all OSPF neighbors to prevent:
- Rogue routers
- Fake OSPF neighbors
- Unauthorized route injection

Authentication Command:

bash
area 0 authentication message-digest


---

# ⚙ Technologies Used

- Cisco IOS
- OSPF
- OSPF MD5 Authentication
- Dynamic Routing
- Cisco Packet Tracer

---

# 🧪 Verification Commands

bash
show ip ospf neighbor
show ip route
show ip protocols
show ip ospf interface g0/1


---

# 📸 Verification Screenshots

- OSPF Neighbor Table
- Routing Table
- Authentication Verification
- Successful Ping Tests
- Final Topology

---

# Skills Demonstrated

- Enterprise Routing
- OSPF Configuration
- OSPF Authentication
- Redundant Routing Design
- Cisco IOS CLI
- Network Troubleshooting
- Routing Security Fundamentals

---

# Project Structure

text
Secure-Enterprise-OSPF-Lab/
│
├── README.md
├── configs/
├── screenshots/
├── topology/
├── packet-tracer/
└── docs/


---

# Author

Junior Network Engineer  
Cisco & Network Security Enthusiast