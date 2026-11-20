
<div align="left">
  <table>
    <tr>
      <td width="130" align="center" valign="middle">
        <img src="Black and White Youtube Profile Picture  (1).png" width="110" alt="MOHTECH Solutions Logo">
      </td>
      <td valign="middle">
        <h1>MOHTECH SOLUTIONS</h1>
        <h3>IT Infrastructure Deployment</h3>
        <p>Windows Server 2019 | Active Directory</p>
      </td>
    </tr>
  </table>
</div>

---

## 01. Project Overview

MOHTECH Solutions is a growing technology company looking to establish and organize its internal IT infrastructure.

As the company expands, it needs a reliable and centralized environment to manage employees, workstations, network services, and access to shared resources.

Taking on the role of an IT administrator, I was tasked with designing and deploying the company's initial IT infrastructure using **Windows Server 2019**.

The project starts with deploying a Windows Server environment and configuring **Active Directory Domain Services (AD DS)** to centrally manage users, computers, and organizational units.

Essential network services are then configured, including **DNS, DHCP, and NAT**, followed by departmental security groups, shared folders with controlled permissions, and Group Policy configurations.

The objective is to simulate the deployment and administration of a small-business IT environment while gaining practical experience in Windows Server administration, networking, access control, and troubleshooting.

## 02. Project Scope

The project covers the following implementation areas:

- Windows Server 2019 deployment
- Active Directory Domain Services (AD DS)
- DNS and DHCP configuration
- NAT and network connectivity
- Organizational Units and security groups
- Departmental file sharing and NTFS permissions
- Group Policy configuration
- PowerShell user provisioning
- Troubleshooting and verification

---

## 03. Lab Environment

The infrastructure was built in a virtualized home lab to simulate a small-business network.

| Component | Configuration |
|:---|:---|
| Server Operating System | Windows Server 2019 |
| Client Operating System | Windows Client VM |
| Domain | ad.mohtechsolutions.test |
| Internal Network | 192.168.10.0/24 |
| Server Internal IP | 192.168.10.10 |
| DHCP Scope | 192.168.10.100 – 192.168.10.200 |
| Server External Interface | DHCP |
| Virtualization | VMware Workstation |

### Network Interfaces

The server uses two network interfaces:

- **External Interface (Internet):** Obtains its IP configuration through DHCP and provides external network connectivity.
- **Internal Interface (Internal):** Uses the static IP address `192.168.10.10` and connects the server to the internal company network.

Windows Server is also configured to provide NAT for internal network connectivity in this lab environment.

---

## 04. Lab Topology

The following diagram illustrates the lab architecture, including the Windows Server, its network interfaces, and the internal company network.

<div align="center">
  <img src="Mohtech-diag.pdf" width="100%" alt="MOHTECH Solutions Network Topology">
  <p><em>Figure 1. MOHTECH Solutions - Network Topology</em></p>
</div>

---

## 05. Infrastructure Implementation

*This section will document the configuration and deployment of the infrastructure components, supported by screenshots and verification results.*

### 05.1 Active Directory Domain Services

### 05.2 DNS and DHCP

### 05.3 Organizational Units and Security Groups

### 05.4 Departmental File Sharing and Permissions

### 05.5 Group Policy Configuration

### 05.6 PowerShell User Provisioning

---

## 06. Troubleshooting and Verification

*Documenting practical issues encountered during implementation, the troubleshooting process, and the solutions applied.*

---

## 07. Skills Demonstrated

- Windows Server Administration
- Active Directory Management
- DNS and DHCP Administration
- Network Configuration and NAT
- Group Policy Management
- NTFS and SMB Permissions
- PowerShell Fundamentals
- IT Troubleshooting
