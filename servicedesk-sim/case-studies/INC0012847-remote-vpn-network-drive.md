# INC0012847 — Remote User Cannot Access Shared Network Drives

**Category:** Network  
**Priority:** High  
**Reported By:** Sarah Mitchell — Marketing, Remote  
**Affected Users:** 1  

---

## Problem
Remote user could not access mapped network drives since that morning.
Receiving "The network path was not found" error. Other office users
could access the drive fine. User had internet and email working normally.

---

## Thought Process
- Other office users unaffected → not a file server issue
- User has internet and email → general connectivity is fine
- User is working remotely → most likely not connected to VPN
- Without VPN, the computer has no tunnel to reach internal file servers
- Drives show disconnected → confirms no path to the server

**Conclusion:** User was not connected to VPN. Without it, the computer
cannot reach internal network resources like file servers even though
internet works fine.

---

## Steps Taken
1. Connected to user's machine via Remote Desktop
2. Checked VPN client — confirmed it was disconnected
3. Opened VPN client and clicked Connect
4. Opened internal documentation to find the Marketing UNC path
   (\\FILESERV01\departments\Marketing)
5. Opened File Explorer → This PC → Map Network Drive
6. Selected drive letter D: and entered the UNC path
7. Confirmed drive mapped successfully and user could access files

---

## Resolution
Connecting VPN and remapping the network drive restored full access
to the Marketing shared drive.

---

## Key Takeaway
Remote users need VPN to reach internal resources. Internet and email
working does not mean VPN is connected — those services route externally.
File servers live on the internal network and are unreachable without
the VPN tunnel. Always check VPN status first for remote users reporting
network drive issues.
