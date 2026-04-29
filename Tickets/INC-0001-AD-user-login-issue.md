# INC-0001 — AD Account Lockout

**Date:** 2026-04-27  
**Priority:** P2 — High  
**Category:** Active Directory  
**Status:** Closed  
**Reported by:** Sara Benhaddou  
**Assigned to:** Nebbak Oussama  
**Resolution time:** 15 minutes  

## Problem
User sara.benhaddou unable to log into domain on PC-01.
Error: "Incorrect password"

## Investigation
1. Checked ADUC on DC-01
2. Account status: Locked Out after 5 failed attempts
3. Root cause identified: incorrect password saved in Edge browser
triggering automatic login attempts

## Root Cause
Incorrect credentials cached in Microsoft Edge browser
automatically retrying and triggering account lockout policy
(threshold: 5 attempts)

## Resolution
1. Verified account in ADUC → DC-01
2. Unlocked account: Unlock-ADAccount -Identity sara.benhaddou
3. Reset temporary password
4. Tested login on PC-01 → Success
5. User informed to clear saved passwords in browser

## Prevention
- User educated on browser credential management
- KB Article created: KB-001

## Lessons Learned
Always check ADUC account status before assuming 
password issue. Lockout and wrong password have 
the same error message for the user.
