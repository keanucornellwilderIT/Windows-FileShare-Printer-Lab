# Windows File Share & Printer Lab

### Overview
This project demonstrates enterprise Windows file sharing, NTFS permission management, mapped drive troubleshooting, and print server administration within an Active Directory environment.

The lab simulates real-world IT support and system administration scenarios involving SMB shares, network printers, access control, printer queues, and connectivity troubleshooting.

### Business Impact:
Resolved access and printing issues impacting end-user productivity across the domain environment.

### Technologies Used
- Windows Server 2022
- Windows 10/11
- Active Directory
- SMB File Sharing
- Print Management
- Remote Desktop

### Key Help Desk Skills Demonstrated
- SMB File Sharing
- NTFS Permission Management
- Printer Administration
- Network Troubleshooting
- Windows Server Administration
- Root Cause Analysis
- Technical Documentation

### Environment Setup
- Windows Server VM
- Windows Client VM
- SMB File Sharing
- Network Printer Access

### Project Configuration Steps
### Step 1 - Configure File Shares
Configured SMB shared folders and verified network access.

### Step 2 - Configure NTFS & Share Permissions
Configured NTFS and share permissions for user access management.

### Step 3- Map Network Drives
Mapped shared folders to client systems and verified connectivity.

### Step 4 - Deploy Network Printers
Configured and shared network printers across the environment.

---

## Help Desk Scenarios

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

## Screenshots
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

## Screenshots

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
Configured Print Server services successfully and deployed printer resources through Print Management for centralized administration within the domain environment.

## Screenshots

### Print Server Role Installation
<img width="784" height="558" alt="image" src="https://github.com/user-attachments/assets/ef87275c-11bb-4b87-a0ef-c85578527fb7" />

### Print Management Console
<img width="950" height="721" alt="image" src="https://github.com/user-attachments/assets/ec651d14-ea91-46ba-8da2-b2ba8dba1b8f" />

### Printer Driver Configuration
<img width="575" height="438" alt="image" src="https://github.com/user-attachments/assets/a8015ca1-8b36-4dca-98e9-f31271efa87e" />

### OfficePrinter Deployment
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

---
### Scenario 4 - Mapped Drive Troubleshooting

#### Problem
`edavis` was unable to access the mapped network drive on `client-1` and could not reach shared company resources within the `CompanyData` folder.

#### Troubleshooting
- Verified connectivity between `client-1` and `dc-1`
- Reviewed mapped drive configuration
- Tested SMB network access using `ping dc-1`
- Verified share permissions and authentication
- Reconfigured mapped drive settings using `\\dc-1\CompanyData`

#### Root Cause
An incorrect network drive mapping prevented `edavis` from accessing shared resources across the domain environment.

## Screenshots

### Broken Network Drive
<img width="859" height="603" alt="image" src="https://github.com/user-attachments/assets/7e8d91af-8ac8-4290-b37a-fea24ef6b567" />

### Connectivity Testing
<img width="517" height="369" alt="image" src="https://github.com/user-attachments/assets/5acee66b-b630-43db-8461-31b4c388da8f" />

### Drive Mapping Configuration
<img width="809" height="472" alt="image" src="https://github.com/user-attachments/assets/e699a241-eba9-4837-b9a9-7537a05c140a" />

### Successful Mapped Drive Access
<img width="909" height="474" alt="image" src="https://github.com/user-attachments/assets/1c20ef1e-4028-447a-8a53-d38117a28421" />


#### Resolution
Reconfigured the mapped network drive and restored successful access to the `CompanyData` shared folder.

#### Skills Learned
- Network drive troubleshooting
- Windows networking
- SMB diagnostics
- Connectivity troubleshooting
- Shared resource management

### Scenario 5 - Printer Queue Troubleshooting

#### Problem
`sjohnson` was unable to print documents because print jobs became stuck within the `OfficePrinter` queue on the print server.

#### Troubleshooting
- Reviewed printer queue status within Print Management
- Verified printer communication and printer status
- Paused and reviewed printer queue activity
- Restarted the Print Spooler service
- Cleared stuck print jobs from the queue
- Tested printer functionality after remediation

#### Root Cause
A print spooler and queue processing issue prevented successful print job completion and caused print jobs to remain stuck within the printer queue.

## Screenshots

### Printer Queue Error
<img width="476" height="282" alt="image" src="https://github.com/user-attachments/assets/92852a57-65e3-4bb5-aa6c-1a8361a36bc2" />

### Print Spooler Service
<img width="844" height="489" alt="image" src="https://github.com/user-attachments/assets/0f0dd24e-5429-4a93-9088-61c5e034558e" />
<img width="379" height="173" alt="image" src="https://github.com/user-attachments/assets/6161d21f-9bd7-4597-a53e-0c43e93dca00" />

### Cleared Printer Queue
<img width="636" height="274" alt="image" src="https://github.com/user-attachments/assets/495476b4-7190-4892-9b77-c5da44f035a7" />

#### Resolution
Cleared the printer queue and restarted the Print Spooler service, restoring normal printing functionality for `sjohnson` and other users within the domain environment.

#### Skills Learned
- Printer troubleshooting
- Print spooler management
- Queue diagnostics
- Windows service management
- End-user support
---

## Lessons Learned
This project improved my understanding of enterprise file sharing and printer management within Windows environments. I learned how to configure secure shared resources, troubleshoot access issues, manage mapped drives, and resolve common printer-related problems encountered in help desk and system administration roles. The lab also strengthened my troubleshooting methodology and documentation skills.
