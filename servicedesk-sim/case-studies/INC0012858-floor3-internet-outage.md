# INC0012858 — Entire Floor 3 Internet Outage (~40 Users)

**Category:** Network  
**Priority:** Critical  
**Reported By:** Eugene Williams — Facilities, Building A Floor 3  
**Affected Users:** ~40  

---

## Problem
All users on Floor 3 lost internet connectivity approximately 30 minutes
before the ticket was filed. Users could ping local resources but could
not reach external websites. Other floors were unaffected. ISP confirmed
no external outages.

---

## Thought Process
- Floor-specific outage → not an ISP or building-wide issue
- Local resources reachable but no external access → switch is up but
  something is wrong with how it's handling traffic
- WiFi access points also affected → rules out a single bad port,
  points to the floor switch itself
- ISP confirmed no outage → problem is internal
- Other floors fine → isolated to Floor 3 switch

**Conclusion:** Floor 3 switch had become unresponsive. A reboot
would force a clean reload and restore full connectivity.

---

## Steps Taken
1. Navigated to Server Room → Devices tab
2. Located Floor 3 Switch in the equipment list
3. Rebooted the switch
4. Waited 30-60 seconds for it to come back online
5. Confirmed with user via Teams that internet was restored for all
   users on Floor 3

---

## Resolution
Switch reboot restored full internet connectivity to all ~40 users
on Floor 3.

---

## Key Takeaway
When an entire floor loses external connectivity but local resources
still respond, the floor switch is the likely culprit. Network switches
can become unresponsive due to memory issues or firmware bugs without
fully powering off — making them appear operational when they are not.
A reboot forces a clean state. Always confirm the fix with the reporter
before closing a critical ticket.
