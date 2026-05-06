# INC0012853 — New Employee Onboarding Access Setup

**Category:** Access  
**Priority:** Medium  
**Requested By:** Robert Torres — HR  
**Affected Users:** 1 (Jennifer Torres, incoming Junior Developer)  

---

## Problem
New hire starting Monday needed an Active Directory account created
and access provisioned to three groups before 9 AM orientation.

---

## Thought Process
- This is a provisioning request, not a break/fix ticket
- Must follow the request exactly — no guessing what access the user needs
- Three specific groups requested: Engineering, VPN-Users, GitHub-Access
- Account must be created before group memberships can be assigned
- SLA is time-sensitive — access needed before start date

**Conclusion:** Create AD account first, then add all three group
memberships exactly as specified in the ticket.

---

## Steps Taken
1. Opened Active Directory
2. Clicked New User and entered Jennifer's details
   - Username: jtorres
   - Name: Jennifer Torres
   - Department: Engineering
   - Manager: Tom Wilson
3. Created the account
4. Searched for jtorres in AD
5. Added to Engineering group
6. Added to VPN-Users group
7. Added to GitHub-Access group
8. Verified all three group memberships were applied

---

## Resolution
Account created and all requested access provisioned ahead of the
Monday 9 AM deadline.

---

## Key Takeaway
New hire onboarding requires two distinct steps — account creation
and group provisioning. Only assign the access that was explicitly
requested. Adding extra groups without approval violates least privilege
principles and creates a security risk. Always complete onboarding
tickets ahead of the start date, a new employee with no access
on day one reflects poorly on the IT team.
