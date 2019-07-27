
# Summary

**Product Name**: Symantec Endpoint Protection Manager Version 14 (14 MP1) .2 build 1023 (14.2.1023.0100) - (older versions may also be affected)

**Impact**:  **High**. A standard windows user (not an admin) can escalate to  **NT SERVICE\semwebsrv**  . With this user role he has access to many of the SEPM components and he can tamper jsp,php and probably jar files. Full takeover of SEPM seems possible.
Moreover, further escalation to SYSTEM is possible. 

**Vulnerability Type**: DLL Preloading

**DLL**: dbicudtx16.dll

**Affected process**: php-cgi.exe

**Attack Vector**: local

# Description

When a user opens the SEPM and tries to login, the php-cgi.exe process is being executed as **NT SERVICE\semwebsrv** and tries to load the **dbicudtx16.dll** from different locations.

One of the directories it searches is  **C:\bin32**  directory . If the directory does not exist, any user can create it and put a malicious dbicudtx16.dll .

The dll will load the next time someone will try to login to the SEPM.

To stress that the directory C:\bin32 does not exist by default, and any user can create folders under C:\ .

# PoC

You can find a full detailed video on the following link:

https://youtu.be/e_hbJ9NdIcg 



**Some time frames of the video:**

00:00 - 00:50 -> identification

00:51 - 02:27 -> attacker's privileges

02:28 - 03:05 -> the attack

03:06 - 03:50 -> triggering the escalation

03:51 - 09:23 -> providing some attack scenarios
