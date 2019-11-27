# Disclosure 
Dear visitor,

**On November 2018**, I informed Symantec for **two vulnerabilities** in **Symantec EndPoint Manager (SEPM)**, which could allow **escalation of privilege (EoP)**. 
**Both vulnerabilities have been verified by Symantec** and **one of them** has been assigned **CVE-2018-18367** (*CVE-2018-18367 PoC*: [https://www.youtube.com/watch?v=d9orQwPMwNE](https://www.youtube.com/watch?v=d9orQwPMwNE) ).
For the CVE-2018-18367, Symantec released an **advisory after 140 days**.

<s>However, **for the second one** and after 8 months (!) of waiting, **there is no advisory yet**.</s>

For this one, on November 14, 2019 Symantec released an advisory and assigned **CVE-2018-18368**. Moreover, they provided credits:
[https://www.symantec.com/security-center/vulnerabilities/writeup/109439?om_rssid=sr-advisories](https://www.symantec.com/security-center/vulnerabilities/writeup/109439?om_rssid=sr-advisories)

<s>Symantec asked for more time to release an advisory, because of their dependency on a component from a 3rd party vendor. Initially, they asked from me to **extend the 90 days disclosure deadline** until **June 2018** (i remind that the **initial report was on November**). oun
These days (**end of July**) they informed me for **a new delay**, and they claimed that the 3rd party vendor, will be ready on **mid to late August**. The vendor has not been revealed to me, because of some kind of NDA, between the vendor and Symantec.
</s>
I have to stress at that point, that I tested the exploitation against **"Symantec EndPoint Manager 14.2.1 (14.2 RU1) build 3332 (14.2.3332.1000)"**, and **it seems that Symantec applied a patch, without waiting for the vendor's fix**. However, they want to wait until the vendor's fix, in order to release the security advisory, thus **there is no advisory yet, after 8 months.**

Being a strong believer of responsible disclosure, and talking into consideration all the above, **I am releasing the details of the second Escalation of Privilege**, in this repository. 

**As far as you have upgraded to the latest release, my guess is that you will have no problems. If you have not upgraded, then probably you are already affected by CVE-2018-18367.**

Hope that i do not cause any inconvenience to the good guys.

Cu around,
gweeperx.
