# INC0012855 — Password Expired After Extended Vacation

**Category:** Access  
**Priority:** High  
**Reported By:** Maria Garcia — Engineering, Building C Floor 3  
**Affected Users:** 1  

---

## Problem
User returned from 3-week vacation to find her password had expired.
System displayed "Your password has expired and must be changed" but
she was unable to change it from the login screen. Sprint deadline
was Friday and she was the lead developer on a critical module.

---

## Thought Process
- Password policy is 90 days — 3 week absence pushed her past expiration
- Cannot change password from login screen because Windows requires
  authentication before allowing a password change
- Account has been with company 4 years — low fraud risk but identity
  must still be verified before any changes
- Temporary password must be communicated securely — never via email
- User must be required to change it on first login

**Conclusion:** Verify identity in AD, reset to a temporary password,
communicate it securely via Teams, require change on next login.

---

## Steps Taken
1. Opened Active Directory
2. Searched for mgarcia (Maria Garcia)
3. Selected her account to open details
4. Sent a verification code to confirm her identity
5. Once verified, clicked Reset Password to generate a temporary password
6. Sent the temporary password to the user securely via Teams chat
7. Informed her she must change it immediately upon login

---

## Resolution
Password reset successfully. User logged in, changed her password,
and regained access to all systems ahead of her sprint deadline.

---

## Key Takeaway
Users returning from extended leave commonly face password expiration
because the 90-day clock keeps running while they are away. They cannot
self-serve the fix because Windows requires authentication to change a
password — creating a catch-22. Always verify identity before resetting,
and always use a secure channel like Teams or phone to share temporary
passwords. Email is never appropriate for transmitting credentials.
