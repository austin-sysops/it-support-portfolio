# INC0012860 — Department Transfer Access Modification

**Category:** Access  
**Priority:** Medium  
**Requested By:** Tom Wilson — Manager  
**Affected Users:** 1 (Kavita Patel, transferring to IT Infrastructure)  

---

## Problem
Employee transferring from Engineering to IT Infrastructure needed
her AD group memberships updated before her first day in the new role.
Old access needed to be revoked and new access provisioned.

---

## Thought Process
- This is an access modification request, not a break/fix ticket
- Two actions required — remove old group AND add new group
- Leaving old group memberships in place is a security violation
- Least privilege principle — users should only have access relevant
  to their current role
- Request came from the manager — authorized source, no further
  verification needed
- Time-sensitive — access needed by Wednesday morning

**Conclusion:** Remove Engineering group membership and add IT
Infrastructure group membership in a single AD update.

---

## Steps Taken
1. Opened Active Directory
2. Searched for kpatel (Kavita Patel)
3. Removed her from the Engineering group
4. Added her to the IT Infrastructure group
5. Verified group memberships were updated correctly

---

## Resolution
Access updated successfully ahead of Kavita's Wednesday start
in the new role.

---

## Key Takeaway
Department transfers are not just about adding new access —
removing old access is equally important. Leaving stale group
memberships is a security risk because the user retains access
to resources they no longer need. This violates least privilege
and creates audit issues. Always treat transfers as a two-step
action: revoke old, grant new.
