# Azure RBAC Configuration Project

## Overview
This project demonstrates how to implement **Role-Based Access Control (RBAC)** in Microsoft Azure using **Azure Entra ID**.  
It showcases the **Principle of Least Privilege** by configuring different access levels for users to an Azure Storage Account.

## Objective
To configure Azure RBAC so that:
- **User1** (in the StorageAdmins group) can access and modify storage resources.
- **User2** (not in the group) is restricted from accessing the storage account.

---

## Steps Taken

### 1. Azure Resource Setup
- Created a **Resource Group** named `RBAC-Project-RG`.
- Created a **Storage Account** named `rbacstorageproject` in the same region.

### 2. Azure Entra ID Configuration
- Created two users:
  - `user1@<tenant>.onmicrosoft.com` (assigned to StorageAdmins group)
  - `user2@<tenant>.onmicrosoft.com` (no access assigned)
- Created a **Security Group** named **StorageAdmins**.

### 3. Role Assignment
- Assigned the **Storage Blob Data Contributor** role to the **StorageAdmins** group at the Storage Account level.

### 4. Testing Access
- Logged in as **User1** → Successfully accessed and uploaded files to the storage account.
- Logged in as **User2** → Access denied to the storage account.

---

## Screenshots
Include screenshots of the following:
1. User creation in Entra ID.
2. Group creation.
3. Role assignment to the group.
4. Successful access by **User1**.
5. Access denied for **User2**.

---

## Key Learnings
- How to manage Azure resources with **Role-Based Access Control (RBAC)**.
- Creating and managing Azure Entra ID users and groups.
- Applying the **Principle of Least Privilege**.
- Testing and validating access permissions in Azure.

---

## Tools Used
- Microsoft Azure Portal
- Azure Entra ID (Identity & Access Management)
- Azure Storage Account
- Web Browser for Portal Access

---

## Duration
**5–6 hours** including setup, testing, and documentation.

---

## Author
**[Your Name]**  
Cloud Security Engineer in Training
