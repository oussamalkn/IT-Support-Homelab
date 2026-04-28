# INC-0002 – Shared Folder Access Denied

## 🧾 Incident Summary
- **Incident ID:** INC-0002  
- **Title:** Access Denied – Finance Shared Folder  
- **User:** sara.benhaddou  
- **Service:** File Sharing (Finance)  
- **Priority:** P2 — High  
- **Status:** Closed  
- **Date:** 2026-04-28  
- **Assigned to:** Nebbak Oussama  
- **Resolution time:** 12 minutes  

---

## 🗣️ User Report
"Since this morning I cannot access the Finance folder 
on the server. I get Access Denied error. It was working yesterday."

---

## 🔍 Diagnostic Process

### Questions asked to user:
1. Since when? → Since this morning
2. Exact error message? → "Access Denied"
3. Any other shared folders accessible? → Yes, only Finance is blocked

### Error message analysis:
- Access Denied → Permission issue confirmed
- Not "Path not found" → Network is fine
- Not login prompt → Credentials are valid

### Investigation on DC-01:
```powershell
Get-ADGroupMember -Identity "GRP-Finance"
```
Result: sara.benhaddou NOT found in group

---

## 🎯 Root Cause
User sara.benhaddou was accidentally removed 
from security group GRP-Finance in Active Directory.
This caused NTFS permission check to fail → Access Denied.

---

## ✅ Resolution Steps
1. Identified missing group membership in ADUC on DC-01
2. Re-added user to group:
```powershell
Add-ADGroupMember -Identity "GRP-Finance" -Members "sara.benhaddou"
```
3. Verified membership:
```powershell
Get-ADGroupMember -Identity "GRP-Finance"
```
4. Tested access from PC-01 with sara.benhaddou → Success

---

## 🛡️ Prevention
- Never remove users from groups without change request
- Quarterly AD group membership audit recommended
- Document all group changes in GLPI

---

## 📚 KB Article
KB-002 — Shared Folder Access Denied: AD Group Membership Check

---

## 💡 Lessons Learned
Access Denied ≠ wrong password.
Always check AD group membership before 
touching NTFS permissions directly.
