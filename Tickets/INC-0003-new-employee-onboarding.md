# INC-0003 – New Employee Onboarding

## 🧾 Incident Summary

* **Type:** Service Request (User Onboarding)
* **User:** Youssef Khalil
* **Department:** Management
* **Priority:** Medium
* **Status:** Resolved
* **Date:** 29/04/2026
* **Resolution time:** 30 minutes

---

## 📋 HR Request

HR requested the onboarding of a new employee, including:

* Creation of Active Directory account
* Assignment to the Management department
* Access to shared network resources
* Workstation preparation before start date

---

## ✅ Actions Performed

### 1. Verified shared resource

* Checked existence of network share:

  ```
  \\192.168.10.2\Management
  ```
* Confirmed the share is accessible

### 2. Verified AD security group

* Confirmed existence of:

  ```
  GRP-Shared-Management
  ```

### 3. Created Active Directory user

```powershell
New-ADUser -Name "Youssef Khalil" `
-SamAccountName "youssef.khalil" `
-UserPrincipalName "youssef.khalil@techmaroc.local" `
-Path "OU=Management,DC=techmaroc,DC=local" `
-Department "Management" `
-Title "Team Lead" `
-AccountPassword (ConvertTo-SecureString "Temp1234!" -AsPlainText -Force) `
-Enabled $true `
-ChangePasswordAtLogon $true
```

### 4. Assigned group memberships

```powershell
Add-ADGroupMember -Identity "GRP-Management" -Members "youssef.khalil"
```

### 5. Verified permissions

* Checked SMB share permissions
* Checked NTFS permissions
* Confirmed group-based access model

### 6. Prepared workstation

* Domain join confirmed
* Required software ready (Office, antivirus)

---

## 🔐 Credentials Delivered

* Temporary password provided via secure communication
* User required to change password at first login

---

## ✔ Verification

* Verified user creation in Active Directory
* Confirmed correct group memberships
* Tested access to shared folder from domain-joined client machine
* No access errors encountered

> ⚠️ Note: Testing from Domain Controller may return false results due to authentication context differences

---

## 💡 Lessons Learned

* Always verify shared resources before granting access
* Use security groups instead of direct user permissions
* Validate SMB access from client machines, not Domain Controllers
* Prefer hostname over IP for reliable authentication (Kerberos)

## 📚 KB Article
KB-003 — New Employee Onboarding Standard Procedure
