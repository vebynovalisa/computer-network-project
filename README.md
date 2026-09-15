# Group 8 - Computer Network Design: Multi-Floor TCP/IP Infrastructure for BINUS Anggrek Building

A computer networking project designing and simulating a multi-floor network infrastructure for the Anggrek Building at BINUS University, covering **Floor 2, Floor 3, and Floor 7**, built using the TCP/IP model with VLSM-based IP allocation, static routing, and application-layer services, fully simulated in **Cisco Packet Tracer**.

## Authors & Contributions

This project was completed collaboratively as an Assurance of Learning (AOL) assignment for the Computer Networks course.

| Name | Student ID |
|---|---|
| Veby Novalisa | 2802552811 |
| Fedryan Ananda Saputra | 2802566363 |
| Luqman Alexsandro Marty Prodi | 2802553682 |
| Zaidan Ikram | 2802551481 |
| Ihsan Panji Rahmawan | 2802550610 |

**Instructor:** Ir. Santoso Budijono, M.M. (D1519)
**Course:** Computer Networks - Odd Semester 2025, BINUS University

## Background

Designing a network for a real, multi-floor building requires more than just connecting devices - it requires understanding room-level device requirements, allocating IP addresses efficiently, and ensuring reliable communication both within and across floors. This project addresses that challenge for three floors of the BINUS Anggrek Building, translating a real floor plan and room requirement dataset into a working, simulated network design.

## Scope

| Aspect | Detail |
|---|---|
| Building | Anggrek Building, BINUS University |
| Floors covered | 2, 3, and 7 |
| Network model | TCP/IP |
| IP addressing | VLSM (Variable Length Subnet Mask) |
| Routing method | Static routing |
| Topology | Tree Topology |
| Simulation tool | Cisco Packet Tracer |

## Approach

The network was designed layer by layer, following the TCP/IP model:

**1. Physical Layer** - Selected UTP Cat 6 (Vascolink Original) cabling for up to 1 Gbps throughput, with VENTION RJ45 Cat6/Cat6A connectors. Cable length per floor was estimated from the floor plan and room layout.

**2. Data Link Layer** - Deployed TP-LINK TL-SG1048 (48-port Gigabit) switches, sized to each room's host requirements (ranging from 25 to 85 hosts per room, typically using /26 and /27 subnets).

**3. Network Layer** - Allocated IP addresses per room using VLSM to minimize address waste, then configured TP-Link TL-ER7206 Omada routers (Core & Distribution roles) with static routing across all three floors.

**4. Transport Layer** - Mapped application services to their respective ports and socket addresses (HTTP/HTTPS, SMTP/POP3, FTP), covering both TCP-based delivery (web, email, FTP) and the role of UDP for latency-sensitive traffic.

**5. Application Layer** - Simulated Web, Email (SMTP/POP3), and FTP services, including a full walkthrough of the email delivery process from client to mail server.

## Key Design Results

| Component | Detail | Cost |
|---|---|---|
| Cabling | UTP Cat 6, 13 rolls (± 3,965 m) | Rp8,240,624 |
| Switches | TP-LINK TL-SG1048, 58 units (Floor 2: 15, Floor 3: 23, Floor 7: 20) | Rp215,180,000 |
| Routers | TP-Link TL-ER7206 Omada, 10 units (Floor 2: 3, Floor 3: 3, Floor 7: 4) | Rp17,000,000 |
| Supporting components | - | Rp22,934,000 |
| **Total estimated cost** | | **Rp263,354,624** |

*Cost estimates based on market prices as of December 2025. End-user devices (e.g., PCs) are not included, as the estimate focuses on network infrastructure only.*

**Validation:** Network connectivity was tested via PING across multiple devices, all of which passed successfully. Web, email, and FTP services were also configured within the simulation.

## File Structure

```
computer-network-project/
├── Proposal_Kelompok_8_AOL_Computer_Networks.pdf   ← Full project report: background, objectives, 5 network layers
├── PPT_AOL_Kelompok_8.pdf                          ← Presentation slides
├── EXCEL_AOL_Kelompok8.xlsx                        ← All supporting calculations
│     Data Peserta                                  ← Team member list
│     Data Job Desk                                 ← Task distribution per member
│     Jumlah Penempatan Tiap Lantai                 ← Device count per floor
│     Harga                                         ← Cost breakdown: cables, switches, routers
│     Pembagian IP                                  ← VLSM-based IP allocation per room
│     Tabel Alokasi IP Address Router               ← Router IP address assignments
│     Routing Table                                 ← Static routing configuration
│     Application Layer                             ← Service & port mapping
│     Testing                                       ← PING & connectivity test results
├── Cisco-Packet-Tracer_AOL_Kelompok8.pkt           ← Full network simulation (3 floors)
└── README.md
```

## Notes

- This is a simulation-based academic project; the network was not physically implemented, but all configurations follow an approach similar to a real-world deployment.
- Room-level device requirements were independently analyzed by the team; the assignment only specified which floors to design for (Floor 2, 3, and 7 of the BINUS Anggrek Building).
