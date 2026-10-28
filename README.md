# AWS VPC Peering Project

##  Project Overview
This project demonstrates private communication between two Amazon Virtual Private Clouds (VPCs) using AWS VPC Peering.

##  Objectives
- Create and configure two VPCs.
- Establish a VPC Peering connection.
- Configure public and private subnets.
- Configure route tables and Security Groups.
- Test connectivity between EC2 instances.

##  AWS Services Used
- Amazon VPC
- Amazon EC2
- VPC Peering
- Internet Gateway
- Route Tables
- Security Groups

##  AWS Region
Mumbai (`ap-south-1`)

##  Network Architecture

### VPC A
- **CIDR Block:** `10.10.0.0/16`
- **Public Subnet:** `10.10.1.0/24`
- **Private Subnet:** `10.10.2.0/24`
- **Bastion Host:** `10.10.1.10`
- **App-A Instance:** `10.10.2.10`
- **Internet Gateway:** Attached to VPC A

### VPC B
- **CIDR Block:** `10.20.0.0/16`
- **Private Subnet:** `10.20.1.0/24`
- **App-B Instance:** `10.20.1.10`

### VPC Peering
A VPC Peering connection enables private communication between VPC A and VPC B using their private IP addresses.

##  Implementation Steps
1. Created VPC A and VPC B.
2. Created public and private subnets.
3. Created and attached an Internet Gateway to VPC A.
4. Created and configured route tables.
5. Created and accepted the VPC Peering connection.
6. Added routes between the two VPCs.
7. Configured Security Groups for SSH and ICMP traffic.
8. Launched EC2 instances.
9. Tested network connectivity using ping and SSH.
10. Tested connectivity failure and recovery by modifying ICMP rules.

##  Testing and Validation
The following tests are included in the project validation:

- Verify that the VPC Peering connection is active.
- Verify route table configurations.
- Test connectivity between EC2 instances using ping.
- Verify SSH connectivity where required.
- Remove an ICMP rule and test connectivity failure.
- Restore the ICMP rule and retest connectivity.


