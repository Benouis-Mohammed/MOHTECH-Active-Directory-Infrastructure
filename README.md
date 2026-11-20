
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

MOHTECH Solutions is a simulated small business requiring a centralized IT infrastructure to manage its employees, workstations, network services, and shared resources.

Taking the role of an IT administrator, I designed and deployed a Windows Server 2019 environment to provide centralized user management, network services, access control, and workstation policies.

The project was implemented in a virtualized home lab using VMware Workstation.

## 02. Lab Environment

| Component | Configuration |
|:---|:---|
| Server OS | Windows Server 2019 |
| Client OS | Windows Client VM |
| Domain | `ad.mohtechsolutions.test` |
| Internal Network | `192.168.10.0/24` |
| Server Internal IP | `192.168.10.10` |
| DHCP Scope | `192.168.10.100 – 192.168.10.200` |
| Virtualization | VMware Workstation |

### Network Topology

The lab uses a dual-network-interface server, connecting the internal company network to external network connectivity through NAT.

<div align="center">
  <img src="MOHTECH-Network-Topology.png" width="85%" alt="MOHTECH Solutions Network Topology">
  <p><em>Figure 1. Lab Network Topology</em></p>
</div>

---

## 03. Infrastructure Implementation

### 3.1 Server and Network Configuration

- Deployed Windows Server 2019.
- Configured external and internal network interfaces.
- Assigned a static IP address to the internal interface.
- Configured NAT to provide internet connectivity to internal clients.
- Installed and configured DNS and DHCP services.

**Server Network Configuration**

<div align="center">
  <img src="IPconfig.png" width="85%" alt="Server network configuration">
</div>

**DNS and DHCP Configuration**

<div align="center">
  <img src="screenshots/01-server-network/dns-dhcp.png" width="85%" alt="DNS and DHCP configuration">
</div>

### 3.2 Active Directory

- Installed Active Directory Domain Services (AD DS).
- Created the domain `ad.mohtechsolutions.test`.
- Created Organizational Units for Employees, Groups, and Computers.
- Organized departmental users and computer accounts.
- Created departmental security groups for IT, HR, Finance, and Sales.

**Active Directory Domain and Organizational Units**

<div align="center">
  <img src="screenshots/02-active-directory/organizational-units.png" width="85%" alt="Active Directory Organizational Units">
</div>

**Departmental Security Groups**

<div align="center">
  <img src="screenshots/02-active-directory/security-groups.png" width="85%" alt="Active Directory Security Groups">
</div>

### 3.3 File Sharing and Access Control

- Created departmental shared folders for IT, HR, Finance, and Sales.
- Configured SMB share permissions and NTFS permissions.
- Assigned access based on departmental security groups.
- Tested access restrictions between departments.

**Departmental Shared Folders and Permissions**

<div align="center">
  <img src="screenshots/03-file-sharing/folder-permissions.png" width="85%" alt="Departmental folder permissions">
</div>

**Access Control Verification**

<div align="center">
  <img src="screenshots/03-file-sharing/access-denied.png" width="85%" alt="Access denied verification">
</div>

### 3.4 Group Policy

- Created and linked a workstation inactivity-lock Group Policy.
- Configured a 10-minute inactivity limit.
- Applied and checked policy settings on the client workstation.

**Group Policy Configuration**

<div align="center">
  <img src="screenshots/04-group-policy/gpo-configuration.png" width="85%" alt="Group Policy configuration">
</div>

**Applied Group Policy Verification**

<div align="center">
  <img src="screenshots/04-group-policy/gpo-verification.png" width="85%" alt="Applied Group Policy verification">
</div>

### 3.5 PowerShell User Provisioning

- Used PowerShell to automate the creation of Active Directory user accounts.

**PowerShell User Provisioning Script**

<div align="center">
  <img src="screenshots/05-powershell/user-provisioning.png" width="85%" alt="PowerShell user provisioning">
</div>

---

## 04. Troubleshooting and Verification

Practical troubleshooting performed during implementation:

- Diagnosed an account login failure caused by a disabled user account.
- Tested departmental folder permissions using different user accounts.
- Refreshed and checked Group Policy application on the client workstation.

---

## 05. Skills Demonstrated

- Windows Server Administration
- Active Directory and Group Policy
- DNS and DHCP Administration
- NAT and Network Configuration
- SMB and NTFS Permissions
- PowerShell Automation
- IT Troubleshooting
