## How many duplicate issues found by canyie?
When a security issue is reported and the report is accepted (the severity rating is determined) or closed as duplicate, the basic information of the report including date of reporting, reporter, severity rating, affected vendor & product and CVE ID will be tracked in the [Issues](https://github.com/canyie/report-tracking/issues) tab.

The tracking process is not guaranteed, and it can be suppressed by either vendor request or myself. Human incapacitation can also lead to out of sync.

## Deadline & Disclosure of Vulnerability Details
Unlike other typical disclosure process, we do not set a deadline in common. In Android world, many vendors just take a very long time fixing every bug. Deadlines become devoid of positive effects as vendors just don't care them. A security issue in Android typically needs 6 months ~ a year to be patched. Setting deadline would just make every bug accessible to attackers before it gets patched.

Vulnerability details are also not guaranteed to be made publicly accessible. However, I may choose to publish it onto [my blog](https://blog.canyie.top/), especially for AOSP bugs which can likely be found in my analysis of monthly android security bulletin. If I decided to publish a complete writeup or PoC, I'll link it to the mirroring issue.

However, for issues specifically affecting certain products, they will be directly publicly disclosed without notifying the affected vendors. Don't ask me why.
