# Enterprise VLAN network with ROAS, DHCP, DNS and ACLs

## Project overview
This project demonstrates the design and implementation of an enterprise-style campus network using VLAN segmentation, Router-on-a-stick, centralized DHCP, DNS services and Access control lists (ACLs)

The network follows the below structure
PCs --> Access switches --> Core Switch --> Router (for intervlan routing)

## VLAN details 
Vlan 10 --> Database --> 192.168.10.0 /24
Vlan 20 --> Admin --> 192.168.20.0 /24
Vlan 30 --> Accounts --> 192.168.30.0 /24
Vlan 40 --> IT --> 192.168.40.0 /24

## Technologies used 
Cisco Packet Tracer
Vlans and dot1q trunking
Router on a Stick (ROAS)
DHCP on Router
DNS
Extended Access Control List (ACLs)

## Security Implementation 
1. Only IT VLAN is allowed to access the Database/DNS Server
2. Admin and Accounts are denied used the ACLS
3. ACLs applied inbound on the Database VLAN sub-interface
4. Server VLAN isolated from the users VLAN

## IP Address Management
DHCP has been configured on the router
Static IP for the DNS server

## Key Takeaways
1. Demonstrates enterprise network design principles
2. Shows understanding of Layer 2 vs Layer 3 roles
3. Emphasizes security, scalability, and simplicity
4. Design aligns with real-world on-prem and cloud networks

## Future Enhancements
- HSRP for gateway redundancy
- OSPF with multiple routers
- NAT and Internet simulation
- Cloud migration using AWS VPC
