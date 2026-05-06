# INC278504 — MFA Codes Not Arriving, User Locked Out

**Category:** Access  
**Priority:** High  
**Reported By:** Emily Watson — HR, Building A Floor 3  
**Affected Users:** 1  

---

## Problem
User's MFA stopped working overnight. Verification codes were not arriving
on her phone despite having signal and restarting her device. Had a project
deadline the same day.

---

## Thought Process
- Phone has signal and was restarted → not a device connectivity issue
- Was working fine until yesterday → likely corrupted or out-of-sync
  authenticator enrollment, not a policy change
- Only fix is to wipe the enrollment and let the user re-enroll fresh
- MFA reset is a sensitive action → identity must be verified first,
  never reset without manager confirmation

**Conclusion:** Reset MFA enrollment in Active Directory after confirming
identity with the user's manager.

---

## Steps Taken
1. Opened Active Directory, searched for ewatson
2. Messaged her manager via Teams to confirm the reset request
3. Received manager confirmation
4. Clicked "Reset MFA" in AD to clear her authenticator enrollment
5. Notified manager that reset was complete
6. User logged in, re-enrolled MFA with a new QR code
7. Confirmed with user via Teams that access was restored

---

## Resolution
MFA enrollment reset successfully. User re-enrolled and regained full
access to all company systems.

---

## Key Takeaway
When MFA codes stop arriving and basic troubleshooting doesn't help,
the authenticator enrollment itself has likely gone out of sync.
The fix is a full reset so the user can re-enroll.
Always verify identity through a manager before resetting MFA —
it is a high-value security action that can be exploited through
social engineering.
