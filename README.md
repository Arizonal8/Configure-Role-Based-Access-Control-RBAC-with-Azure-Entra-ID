# Azure RBAC Configuration Project

## Overview
This project demonstrates how to implement **Role-Based Access Control (RBAC)** in Microsoft Azure using **Azure Entra ID**.  
It showcases the **Principle of Least Privilege** by configuring different access levels for users to an Azure Storage Account.

## Objective
To configure Azure RBAC so that:
- **User1(Mark)** (in the StorageAdmins group) can access and modify storage resources.
- **User2(Dora)** (not in the group) is restricted from accessing the storage account.

---

## Steps Taken

### 1. Azure Resource Setup
- Created a **Resource Group** named `Meltechresourcegrp`.
- Created a **Storage Account** named `Meltechstorageaccount` in the same region.
-  Created a **Virtual Machine** named `Meltechvmachine`.

### 2. Azure Entra ID Configuration
- Created two users:
  - `Mark_User1@fortuneihekwemegmail.onmicrosoft.com` (assigned to StorageAdmins group)
  - `Dora_User2@fortuneihekwemegmail.onmicrosoft.com` (no access assigned)
- Created a **Security Group** named **Meltechgrp**.

### 3. Role Assignment
- Assigned the **Storage Blob Data Contributor** role to the **Meltechstorageaccount** group at the Storage Account level.
- Assigned the **Virtual Machine Administrator Login** role to the **MeltechVirtual Machine**.

### 4. Testing Access
- Logged in as **User1(Mark)** → Successfully accessed and uploaded files to the storage account.
-  Logged in as **User1(Mark)** → Successfully accessed the resources in the virtual machine.
- Logged in as **User2(Dora)** → Access denied to the storage account.

---

## Screenshots
Include screenshots of the following:
1. User creation in Entra ID.
2. Group creation.
3. Role assignment to the group.
4. Successful access by **User1(Mark)**.

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

