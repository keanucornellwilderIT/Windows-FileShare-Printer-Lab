# Windows File Share & Printer Lab

## 📌 Overview
This project simulates enterprise-level file sharing and printer management within a Windows environment. The lab focuses on configuring shared folders, managing NTFS and share permissions, troubleshooting mapped drives, deploying printers, and resolving printer queue issues commonly handled by IT support and system administrators.

The goal of this project is to build practical experience with file services, printer administration, access management, and real-world help desk troubleshooting workflows in enterprise environments.

## 🎯 Objectives
- Configure enterprise file shares
- Manage NTFS and share permissions
- Troubleshoot mapped drive issues
- Deploy and manage network printers
- Resolve printer queue and connectivity issues
- Practice real-world help desk troubleshooting workflows

## 🧰 Technologies Used
- Windows Server 2022
- Windows 10/11
- Active Directory
- SMB File Sharing
- Print Management
- Remote Desktop

## 🏗️ Environment Setup
- Windows Server VM
- Windows Client VM
- Domain Environment
- SMB File Sharing
- Network Printer Access

## ⚙️ Project Configuration Steps
### Step 1 - Configure File Shares
Configured SMB shared folders and verified network access.

### Step 2 - Configure NTFS & Share Permissions
Configured NTFS and share permissions for user access management.

### Step 3- Map Network Drives
Mapped shared folders to client systems and verified connectivity.

📸 Screenshot here

### Step 4 - Deploy Network Printers
Configured and shared network printers across the environment.

Screenshot here
 
---

## 🛠️ Help Desk Scenarios

### Scenario 1 - SMB File Share Configuration

#### Problem
`sjohnson` required centralized access to company files stored within the shared `CompanyData` folder on `dc-1`.

#### Troubleshooting
- Created the `CompanyData` shared folder
- Configured SMB sharing settings
- Configured share-level permissions for `Domain Users`
- Verified network accessibility from `client-1`
- Tested user connectivity to `\\dc-1\CompanyData`

#### Root Cause
Shared file resources required proper SMB configuration and network access permissions before users could access company data across the domain environment.

## 📸 Screenshots
### Created Shared Folder `CompanyData`
<img width="1319" height="705" alt="image" src="https://github.com/user-attachments/assets/1efbfed3-d171-4ab2-8c52-83284ac0f76c" />

### SMB Share Configuration
<img width="361" height="444" alt="image" src="https://github.com/user-attachments/assets/1238b655-1f0a-4372-b86a-b12b7149eaa5" />

### Share Permissions Configuration
<img width="362" height="484" alt="image" src="https://github.com/user-attachments/assets/95a2ffa3-3006-446d-b987-888ebad5078d" />

### Client Share Access
<img width="1124" height="627" alt="image" src="https://github.com/user-attachments/assets/bf1dc9f1-5293-45ce-811f-2e1c8d72ee48" />



#### Resolution
Configured SMB file sharing successfully and verified that users could access the shared folder across the network environment.

#### Skills Learned
- SMB file sharing
- Windows file services
- Network resource configuration
- User access management
---

### Scenario 2 - NTFS & Share Permissions

#### Problem
`sjohnson`, a member of the `HR Users` group, was unable to modify files within the shared `CompanyData` folder even though she was expected to have modification access.

#### Troubleshooting
- Reviewed NTFS permissions on the shared folder
- Checked share-level permissions
- Verified `sjohnson` group membership
- Tested effective permissions
- Reviewed role-based access settings
- Investigated inherited permissions and group access conflicts

#### Root Cause
The `HR Users` group only had `Read & Execute` permissions configured on the shared folder, preventing users from modifying files.

## 📸 Screenshots

### NTFS Permissions Before Fix
<img width="362" height="449" alt="image" src="https://github.com/user-attachments/assets/d4dcd2e9-02cd-4940-a06b-3847653ee6c4" />

### Access Denied Test
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/005d901c-e918-4574-b0b9-14a793e8c0ff" />

### IT Admin Permission Review
<img width="361" height="453" alt="image" src="https://github.com/user-attachments/assets/041b0a5c-58e7-499d-9f51-1e42a752d606" />

### HR Users Modify Permission
<img width="359" height="447" alt="image" src="https://github.com/user-attachments/assets/31130efd-34f5-4fea-9a92-40ecf8bc9f9a" />

#### Resolution
Permissions were reviewed and updated to grant the `HR Users` group `Modify` access. After permissions were corrected, `sjohnson` successfully modified files within the shared folder.

#### Skills Learned
- NTFS permission troubleshooting
- Share permission management
- Active Directory group administration
- Access control troubleshooting
- Windows file share administration
- Effective permissions analysis

---

### Scenario 3 - Print Server Deployment

#### Problem
The organization required centralized printer deployment and management within the domain environment.

#### Troubleshooting
- Installed Print and Document Services role
- Configured Print Server services on `dc-1`
- Added and configured printer resources
- Verified printer deployment settings within Print Management

#### Root Cause
Print services and printer resources required centralized deployment configuration before network-based printer management could be performed.
## 📸 Screenshots

### Print Server Role Installation
<img width="784" height="558" alt="image" src="https://github.com/user-attachments/assets/ef87275c-11bb-4b87-a0ef-c85578527fb7" />

### Print Management Console
<img width="368" height="547" alt="image" src="https://github.com/user-attachments/assets/7f84ddcb-f6d5-455a-a993-1646c581123d" />
<img width="950" height="721" alt="image" src="https://github.com/user-attachments/assets/ec651d14-ea91-46ba-8da2-b2ba8dba1b8f" />

### Printer Driver Configuration
<img width="575" height="438" alt="image" src="https://github.com/user-attachments/assets/a8015ca1-8b36-4dca-98e9-f31271efa87e" />

### OfficePrinter Deployment
<img width="575" height="438" alt="image" src="https://github.com/user-attachments/assets/e136cdf2-1de4-4216-9cd5-0742446b22c8" />
<img width="574" height="435" alt="image" src="https://github.com/user-attachments/assets/4d389dd3-4d58-40d4-baf1-130eea8ce527" />
<img width="944" height="211" alt="image" src="https://github.com/user-attachments/assets/f1202338-01d7-4752-b6e9-a2bfbc2c7671" />

#### Resolution
Configured Print Server services successfully and deployed printer resources through Print Management for centralized administration.

#### Skills Learned
- Print Server administration
- Printer deployment
- Windows Server management
- Print Management configuration
- Enterprise printer services

### Scenario 4 - Print Server Deployment

#### Problem
Organization required centralized printer deployment and management.

#### Troubleshooting
- Installed printer drivers
- Configured shared printers
- Verified print server communication
- Connected client devices

#### Root Cause
Printer resources required centralized deployment configuration.

Screenshot here

#### Resolution
Successfully deployed shared network printers through print server configuration.

#### Skills Learned
- Print server management
- Printer deployment
- Driver installation
- Network printer configuration
---

### Scenario 5 - Printer Queue Troubleshooting

#### Problem
Print jobs were stuck in the printer queue and users could not print.

#### Troubleshooting
- Reviewed print queue status
- Restarted print spooler service
- Cleared stuck print jobs
- Verified printer connectivity

#### Root Cause
Print spooler/queue issue preventing successful print job processing.

Screenshot here

#### Resolution
Cleared printer queue and restored normal printing operations.

#### Skills Learned
- Printer troubleshooting
- Print spooler management
- Queue diagnostics
- End-user support
---

## 🧠 Key Help Desk Skills Demonstrated
- SMB File Sharing
- NTFS Permission Management
- Printer Administration
- Network Troubleshooting
- Windows Server Administration
- Root Cause Analysis
- Technical Documentation

## 📖 Lessons Learned
This project improved my understanding of enterprise file sharing and printer management within Windows environments. I learned how to configure secure shared resources, troubleshoot access issues, manage mapped drives, and resolve common printer-related problems encountered in help desk and system administration roles. The lab also strengthened my troubleshooting methodology and documentation skills.
