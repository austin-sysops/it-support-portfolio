# INC0012870 — All 12 Network Printers Offline Building-Wide

**Category:** Server  
**Priority:** High  
**Reported By:** Dorothy Martinez — Legal, Building A  
**Affected Users:** Entire building  

---

## Problem
Every network printer in the building showed "Offline" status with
print jobs stuck in queue. All 12 printers affected simultaneously.
Print server PRINT01 was not responding to ping. Last known good
state was the previous evening at 6 PM.

---

## Thought Process
- All 12 printers offline simultaneously → not individual printer issues
- All printers depend on a single print server — PRINT01
- PRINT01 not responding to ping → server is down or frozen
- Last known good was 6 PM yesterday → something happened overnight,
  likely the print spooler service crashed or the server froze
- Rebooting PRINT01 will restart the print spooler and bring all
  printers back online at once
- High-priority departments affected — Legal needs to print contracts,
  Executives need presentations

**Conclusion:** PRINT01 had crashed or frozen overnight. A reboot
would restore the print spooler and bring all 12 printers back online.

---

## Steps Taken
1. Navigated to Server Room → Servers tab
2. Located PRINT01 in the server list
3. Confirmed status showed as Down
4. Clicked Reboot to restart the print server
5. Waited for PRINT01 to come back online
6. Confirmed with user via Teams that printing was restored

---

## Resolution
Print server reboot restored all 12 network printers simultaneously.
Building-wide printing returned to normal.

---

## Key Takeaway
A print server is a single point of failure for all network printing.
When every printer goes offline at once, the print server is always
the first thing to check — not the individual printers. A server
that won't respond to ping is typically frozen or crashed and needs
a reboot. After the server comes back up, users with stuck print
jobs may need to clear their queues manually before printing again.
