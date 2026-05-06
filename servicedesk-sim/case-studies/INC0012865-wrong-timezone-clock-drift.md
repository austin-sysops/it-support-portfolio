# INC0012865 — Wrong Timezone and Clock Drift Causing Missed Meetings

**Category:** Software  
**Priority:** High  
**Reported By:** Kevin Park — Sales, Building A Floor 2  
**Affected Users:** 1  

---

## Problem
User's computer was set to Eastern Time instead of Central Time and
the clock was running approximately 2 minutes fast. This caused calendar
invites, Teams meeting times, and file timestamps to all display
incorrectly. User had already missed meetings and had three more
scheduled that afternoon.

---

## Thought Process
- Two separate issues — wrong timezone AND clock drift
- These require two different fixes, not one
- Timezone is a settings change — Control Panel or Settings app
- Clock drift is fixed by syncing with the company time server
- User already restarted with no change → not a temporary glitch,
  needs manual correction
- Remote desktop is the fastest way to fix this without walking
  the user through it step by step
- Time-sensitive — three more meetings that afternoon

**Conclusion:** Connect via remote desktop, correct the timezone,
then sync the clock with the time server. Both steps required.

---

## Steps Taken
1. Connected to user's machine via Remote Desktop
2. Opened Settings → Time & Language
3. Changed timezone from Eastern to Central Time
4. Clicked Sync Clock Now to correct the 2-minute drift
5. Verified both the timezone and clock displayed correctly

---

## Resolution
Timezone corrected to Central Time and clock synced successfully.
User's calendar invites and meeting times displayed correctly going
forward.

---

## Key Takeaway
Timezone and clock drift are two distinct problems that require
two separate fixes. Changing the timezone does not fix clock drift,
and syncing the clock does not fix the timezone. Both must be
addressed or the user will still experience issues. Always use
remote desktop for time-sensitive fixes rather than walking users
through multi-step processes — it is faster and less error-prone.
