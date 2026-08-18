## How many duplicate issues found by canyie?
When a security issue is reported and the report is accepted (the severity rating is determined) or closed as duplicate, the basic information of the report including date of reporting, reporter, severity rating, affected vendor & product and CVE ID will be tracked in the [Issues](https://github.com/canyie/report-tracking/issues) tab.

The tracking process is not guaranteed, and it can be suppressed by either vendor request or myself. Human incapacitation can also lead to out of sync.

## Deadline & Disclosure of Vulnerability Details
Unlike other typical disclosure process, we do not set a uniform deadline in common. In Android world, many vendors just take a very long time fixing every bug. Deadlines become devoid of positive effects as vendors just don't care them. A security issue in Android typically needs 6 months ~ a year to be patched. Setting deadline would just exposes every bug to attackers before it gets patched.

Vulnerability details are also not guaranteed to be made publicly accessible. However, I may choose to publish it onto [my blog](https://blog.canyie.top/), especially for AOSP bugs which can likely be found in my analysis of monthly android security bulletin. If I decided to publish a complete writeup or PoC, I'll link it to the mirroring issue.

However, for issues specifically affecting certain products, they will be directly publicly disclosed without notifying the affected vendors. Don't ask me why.

## What to report
In short words: any potential issues that could constitute a security vulnerability. 

We are also interested in issues that do not qualify as security vulnerability but do have security implications, e.g. mitigation bypasses that require another vulnerability to exploit, social engineering, or phishing attacks. Sometimes they are reported to affected vendors in order to allow vendors to take actions to harden against such attacks, but if the vendors don't consider them to be vulnerabilities, they are usually won't be tracked here. However, they may be publicly disclosed in other channels like [my blog](https://blog.canyie.top/).

## Recommended Severity Rating
The recommended security severity rating is determined based on the vendor's published severity classification rules, but absolute consistency with the vendor's rating is not pursued. For bugs that could be exploited in an extremely simple way (that is, the malicious actor could reliably perform the attack with little user interaction), and successful exploitation could result in disastrous system breach across the system's critical security boundaries, a higher severity rating might apply. 

Web services examples: logging into any account, resetting any account's password, accessing large amount of sensitive data or personally identifiable information (PII), dropping an entire database resulting in significant data loss, etc.

Client devices examples: silently activating accessibility services or screen recording, accessing various highly sensitive user data from multiple sources, [obtaining multiple sensitive runtime/special permissions without explicit user consent](https://github.com/canyie/CVE-2024-23700), etc.

## Methodology
Most issues are found by human or fuzz testing. If AI was used during the discovery of a bug, the methodology section will indicate "AI assisted".
