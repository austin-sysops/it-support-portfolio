# INC221823 — Entire Floor Lost Internet After Power Flicker

**Category:** Network  
**Priority:** Critical  
**Reported By:** Jessica Tran — Engineering, Building A Floor 1  
**Affected Users:** ~30  

---

## Problem
After a brief power flicker, all users on Floor 1 lost internet connectivity.
Both wired and wireless affected. Other floors were fine. Power had returned
but internet had not.

---

## Thought Process
- Outage was floor-specific → not an ISP issue, not a building-wide problem
- Both wired and wireless affected → rules out a single bad cable or WiFi issue
- Power event preceded the outage → network switch likely entered a fault state
- Other floors unaffected → isolated to the Floor 1 switch

**Conclusion:** Floor 1 switch needed a reboot to reload its firmware cleanly.

---

## Steps Taken
1. Navigated to Server Room → Devices tab
2. Located Floor 1 Switch
3. Rebooted the switch
4. Confirmed with user via Teams chat that internet was restored

---

## Resolution
Switch reboot restored full connectivity to all ~30 users on Floor 1.

---

## Key Takeaway
Power surges can cause switches to enter a fault state even after power
returns. A clean reboot forces firmware reload and restores port connectivity.
When an entire floor loses network access after a power event, the floor
switch is the first thing to check.
