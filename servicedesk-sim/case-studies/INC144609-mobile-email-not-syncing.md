# INC144609 — Mobile Email Not Syncing

**Category:** Software  
**Priority:** Medium  
**Reported By:** Laura Santos — Finance, Building A Floor 1  
**Affected Users:** 1  

---

## Problem
User's company email stopped syncing on her phone overnight. Showing
"Cannot connect to server" error. Email worked fine on her laptop.

---

## Thought Process
- Email works on laptop → account is active, no server-side issue
- Phone has internet and other apps work → not a connectivity issue
- Only the phone email app is broken → problem is isolated to the app itself
- Stopped working overnight → likely a corrupted cache, bad token,
  or app update glitch
- No need to touch server settings — original config was correct

**Conclusion:** The email app on the phone got into a bad state.
Reinstalling clears local corruption and re-syncs cleanly.

---

## Steps Taken
1. Asked user via Teams if email worked on any other device
2. User confirmed email worked fine on laptop — account was healthy
3. Instructed user to uninstall the email app from their phone
4. User reinstalled from the app store and signed back in
5. Confirmed email syncing resumed normally

---

## Resolution
Reinstalling the email app resolved the sync issue immediately.

---

## Key Takeaway
When only one device is affected and the account works elsewhere,
the problem is always local to that device — not the server or account.
Reinstalling the app is faster and more reliable than walking a user
through manual server settings, especially when the original config
was working correctly.
