# Enterprise Network-Implementation.
500 Users, 5 VLANs, 1 Bulletproof Network
### Project Objective
Design, implement, and optimize a secure, high-performance network infrastructure for a growing mid-sized company with 500 users across multiple departments, supporting both on-site and remote work environments. The project aims to improve network security, performance, and manageability while accommodating future growth.

#**End Goals**
- A fully operational LAN with proper segmentation and security measures.
- Configured and optimized network devices (router, switch, access points).
- A functioning VPN solution for secure remote access.
- Implemented network monitoring and management tools.
- Comprehensive documentation of the network setup, including diagrams and procedures.
- A disaster recovery and future expansion plan.
### Skills Learned
- Network Design and Planning: Creating efficient network topologies, IP addressing and subnetting.
- Hardware Configuration: Router setup and Managed switch configuration, Wireless access point deployment.
- Network Protocols and Services: DHCP server configuration, DNS management, VLAN implementation and inter-VLAN routing.
- Network Security: Firewall configuration and management, Implementing port security on switches, Setting up and managing VPNs, Configuring access control lists (ACLs).
- Performance Optimization: Quality of Service (QoS) implementation, Network traffic analysis and optimization using Wireshark, troubleshooting using the COMPTIA approach.
- Disaster Recovery and Business Continuity: Developing backup and recovery strategies; Creating and testing failover procedures.
### Tools Used
**Hardware:**
- Router: Cisco RV340 Dual WAN Gigabit VPN Router
- Switch: Cisco SG350-28 28-Port Gigabit Managed Switch
- Access Point: Ubiquiti UniFi AC Pro
- Server: Dell PowerEdge R640 (for hosting services and VMs)
- Workstations: Various laptops and desktops for testing

**Software and Operating Systems**:
- pfSense (open-source firewall/router software)
- VMware ESXi (hypervisor for server virtualization)
- Windows Server 2019 (for Active Directory and file services)
- Ubuntu Server 20.04 LTS (for various network services)
- OpenVPN (for VPN implementation)

**Network Monitoring and Management:**
- Nagios Core (for network monitoring and alerting)
- Wireshark (for packet analysis and troubleshooting)
- PRTG Network Monitor (for comprehensive network monitoring)

**Documentation and Diagramming:**
- Microsoft Visio (for network diagramming)
- Draw.io (free alternative for creating network diagrams)
- IT Glue (for documentation management)

**Security Tools**:
- Nmap (for network discovery and security auditing)
- Kali Linux (for penetration testing and security assessments)
- Snort (for intrusion detection and prevention)

**Automation and Scripting:**
- PowerShell (for Windows automation and scripting)
- Ansible (for configuration management and automation)
- Git (for version control of configuration files and scripts)

**Backup and Recovery:**
- Veeam Backup & Replication (for VM and data backup)
- Clonezilla (for disk imaging and cloning)

**Miscellaneous:**
- PuTTY (SSH and telnet client)
- WinSCP (SFTP client for file transfers)
- Slack (for team communication and alerts integration)
  
### Step 1: Planning and Design

Define the network topology (e.g., star topology)
Determine IP addressing scheme (e.g., 192.168.1.0/24 for LAN)
List required equipment (e.g., router, switch, access points, cables)
Create a network diagram using a tool like draw.io or Visio

Step 2: Setting up the Local Area Network (LAN)

Configure the main router

Set up WAN connection
Configure LAN IP address and DHCP server
Enable basic security features (e.g., firewall)


Set up and configure the switch

Connect to router's LAN port
Configure VLANs if needed


Set up Wi-Fi access points

Connect to switch
Configure SSID and security settings



Step 3: Configuring Network Devices

Router configuration

Set up port forwarding for specific services
Configure Quality of Service (QoS) settings
Enable logging and monitoring


Switch configuration

Set up port security
Configure Spanning Tree Protocol (STP)
Set up link aggregation (if applicable)


Implement network segmentation

Create VLANs for different departments or purposes
Configure inter-VLAN routing on the router



Step 4: Implementing and Managing VPN

Choose a VPN protocol (e.g., OpenVPN, IPsec)
Configure VPN server on the router or a dedicated device
Set up client configurations
Test VPN connectivity from outside the network

Step 5: Network Monitoring and Management

Set up a network monitoring tool (e.g., Nagios, PRTG)
Configure alerts for downtime or performance issues
Implement a log management solution

Step 6: Documentation

Create a detailed network map
Document IP addressing scheme and VLAN assignments
Write standard operating procedures for common tasks
Create a troubleshooting guide

Step 7: Testing and Optimization

Conduct thorough testing of all network components
Perform a security assessment
Optimize network performance based on findings
Document test results and optimizations made

Step 8: Disaster Recovery Planning

Set up a backup system for network configurations
Create a failover plan for critical network components
Document the disaster recovery process

Step 9: Future Expansion Planning

Identify potential areas for network growth
Plan for scalability in future equipment purchases
Document recommendations for future upgrades
