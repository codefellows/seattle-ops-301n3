# 301 Project Requirements

## Remote Access:
- Implement a Virtual Private Network solution
- Implement some sort of network access control system
  - RADIUS

## AD Automation:
- Create a PowerShell script that automates the following tasks
  - Assigns the Windows Server VM a static IPv4 address
  - Assigns the Windows Server VM a DNS
  - Renames the Windows Server VM
  - Installs AD-Domain-Services
  - Creates an AD Forest
- User and Group Management:
  - Use PowerShell to automate the creation, deletion, and modification of user accounts and groups in AD. Include generation or usernames, passwords, group assignment based on roles and modify group membership as needed
- Group Policy Management:
  - Use PowerShell to automate the management of GPOs in AD, could include creation and deployment of GPOs, enforce security settings, and audit of GPO configurations
- Group Membership Auditing:
  - Use PowerShell to automate the auditing of group membership in Active Directory. The script can generate reports on group membership changes, track which users have been added or removed from specific groups, and monitor for suspicious changes.
- Automate Security Group Management: Use PowerShell to automate the management of security groups in Active Directory.  Script could automatically assign permissions to security groups based on user roles, audit security group membership, and enforce security policies.
- Automate Active Directory Object Cleanup: Use PowerShell to automate the cleanup of stale or unused objects in Active Directory. Script could identify and delete inactive user accounts, computers, or other objects that are no longer needed.

## Network Security Automation
- Firewall Rules Based on AD Groups: Use AD Groups to create FW rules that restrict access to specific resources based on user roles and responsibilities. Use PowerShell to automate the creation and management of these rules
- Firewall Policies for remote workforce: Use PowerShell to implement firewall policies that are tailored for remote workforce accessing corporate resources via VPN
- Automate VPN Client Deployment: Use PowerShell to automate the deployment of VPN clients to end-user devices. This involves the download and install of VPN clients, and configuring VPN client settings based on user roles and responsibilities
