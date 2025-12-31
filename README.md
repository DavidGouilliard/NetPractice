*This project has been created as part of the 42 curriculum by dagouill.*

---

# Description

This project focuses on understanding **networking fundamentals** through the NetPractice training interface.

Each level requires configuring a virtual network correctly so that all hosts can communicate as expected.

---
# Instructions

1. Open `index.html` with web browsrer (doesn't work with Firefox).
2. Complete each level by configuring IP addresses, subnet masks and routing elements correctly.
3. Once a level is completed, **export the configuration** using the interface export option.
4. You must export **10 configuration files**, one for each level.
5. All exported files must be placed **at the root of the Git repository**.

---
# Resources

This section lists references used to study the networking concepts required for NetPractice.

## TCP/IP addressing

### TCP : Transmission Control Protocol

Network protocol that lets two hosts connect and exchange data streams.
TCP ensures packets are reliably delivered and error-free.

TCP ensures **congestion control**, which means the initial requests start small,
increasing in size to the levels of bandwidth computers, servers, network can support.
https://developer.mozilla.org/en-US/docs/Glossary/TCP

### IP : Internet Protocol

An IP address is a numerical lablel assigned to device connected to a network
which uses Internet Protocol for communication.

IP adress can be :
- IPv4, 32-bit, divded into 4 blocks.
    exampe : `192.0.2.1`
- IPv6, 128-bit, divided into 8 blocks.
    example : `2001:db8:3333:4444:5555:6666:7777:8888`
https://en.wikipedia.org/wiki/IP_address

### Reserved IP adresses

- Loopback (used by host to test networking to itself) :
    `127`
- Reserved :
    `10`, `172`, `192`
https://en.wikipedia.org/wiki/Reserved_IP_addresses

### Network, Broadcast and Host

- **Network** : first IP, identifies subnet itself.
- **Broadcast** : last IP, used to deliver packet to all hosts in subnet.
- **Host** : usuable IP whithin subnet.

## Netmasks and subnets

### Subnetting

Process of dividing a network into smaller network section.

### Subnet mask

portion of an IP address that defines the network, as opposed to identifying a particular computer.

### Classless Inter-Domain Routing (CIDR)

Notation where mask is defined as bits after /

| CIDR | Addresses | Hosts | Netmask           | Amount of a Class C |
|------|-----------|-------|-------------------|---------------------|
| /30  | 4         | 2     | 255.255.255.252   | 1/64                |
| /29  | 8         | 6     | 255.255.255.248   | 1/32                |
| /28  | 16        | 14    | 255.255.255.240   | 1/16                |
| /27  | 32        | 30    | 255.255.255.224   | 1/8                 |
| /26  | 64        | 62    | 255.255.255.192   | 1/4                 |
| /25  | 128       | 126   | 255.255.255.128   | 1/2                 |
| /24  | 256       | 254   | 255.255.255.0     | 1                   |
| /23  | 512       | 510   | 255.255.254.0     | 2                   |
| /22  | 1024      | 1022  | 255.255.252.0     | 4                   |
| /21  | 2048      | 2046  | 255.255.248.0     | 8                   |
| /20  | 4096      | 4094  | 255.255.240.0     | 16                  |
| /19  | 8192      | 8190  | 255.255.224.0     | 32                  |
| /18  | 16384     | 16382 | 255.255.192.0     | 64                  |
| /17  | 32768     | 32766 | 255.255.128.0     | 128                 |
| /16  | 65536     | 65534 | 255.255.0.0       | 256                 |

https://www.aelius.com/njh/subnet_sheet.html

## OSI (Open Systems Interconnection) reference model

Divides network communication into 7 abstract layers.

| OSI Layer | Name           | Description |
|----------|----------------|-------------|
| Layer 7  | Application    | User-facing network services and protocols    |
| Layer 6  | Presentation   | Data formatting, encryption, compression |
| Layer 5  | Session        | Connection setup, management and teardown |
| Layer 4  | Transport      | Data delivery |
| Layer 3  | Network        | Addressing, routing between networks|
| Layer 2  | Data Link      | Data transfert whithin same network |
| Layer 1  | Physical       | Physical transmission of raw bits |

https://www.ibm.com/think/topics/osi-model

---

# Use of AI

AI tools were used as a **learning aid** to:
- Rephrase and clarify theorical explanation
- Improve the structure and formatting of this README
- Validate understanding of networking concepts

All configuration work and problem solving were performed manually by the author.
