# 🔧 Router Configurations — Secure Enterprise OSPF Lab

## 🛠 R1 Configuration

```bash
enable
configure terminal

hostname R1

interface g0/0
ip address 192.168.10.1 255.255.255.0
no shutdown

interface g0/1
ip address 10.0.13.1 255.255.255.252
no shutdown

interface g0/2
ip address 10.0.12.1 255.255.255.252
no shutdown

interface g0/1
ip ospf message-digest-key 1 md5 Cisco123

interface g0/2
ip ospf message-digest-key 1 md5 Cisco123

router ospf 1
router-id 1.1.1.1
area 0 authentication message-digest

interface g0/0
ip ospf 1 area 0

interface g0/1
ip ospf 1 area 0

interface g0/2
ip ospf 1 area 0
```

## 🛠 R2 Configuration

```bash
enable
configure terminal

hostname R2

interface g0/0
ip address 192.168.20.1 255.255.255.0
no shutdown

interface g0/1
ip address 10.0.23.1 255.255.255.252
no shutdown

interface g0/2
ip address 10.0.12.2 255.255.255.252
no shutdown

interface g0/1
ip ospf message-digest-key 1 md5 Cisco123

interface g0/2
ip ospf message-digest-key 1 md5 Cisco123

router ospf 1
router-id 2.2.2.2
area 0 authentication message-digest

interface g0/0
ip ospf 1 area 0

interface g0/1
ip ospf 1 area 0

interface g0/2
ip ospf 1 area 0
```

## 🛠 R3 Configuration

```bash
enable
configure terminal

hostname R3

interface g0/0
ip address 192.168.30.1 255.255.255.0
no shutdown

interface g0/1
ip address 10.0.13.2 255.255.255.252
no shutdown

interface g0/2
ip address 10.0.23.2 255.255.255.252
no shutdown

interface g0/1
ip ospf message-digest-key 1 md5 Cisco123

interface g0/2
ip ospf message-digest-key 1 md5 Cisco123

router ospf 1
router-id 3.3.3.3
area 0 authentication message-digest

interface g0/0
ip ospf 1 area 0

interface g0/1
ip ospf 1 area 0

interface g0/2
ip ospf 1 area 0
```
