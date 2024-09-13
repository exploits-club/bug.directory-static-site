tags: #windows #lpe #learning_resource
original link: [Breaking Barriers and Assumptions: Techniques for Privilege Escalation on Windows: Part 3](https://www.zerodayinitiative.com/blog/2024/7/31/breaking-barriers-and-assumptions-techniques-for-privilege-escalation-on-windows-part-3?ref=blog.exploits.club)
newsletter link: [exploits.club Weekly Newsletter 33 - CPU Vulns, Breaking Samsung Bootloaders, Tony Hawk Pro Skater, And More](https://blog.exploits.club/exploits-club-weekly-newsletter-33-cpu-vulns-breaking-samsung-bootloaders-tony-hawk-pro-skater-and-more-2/)

---
## Exploits Club Summary:
> [ZDI](https://www.zerodayinitiative.com/?ref=blog.exploits.club) is back this week with their third installment of the ongoing **Windows PrivEsc series, this time discussing a technique for leveraging an on-boot delete primitive to abuse the Windows Task Scheduler.** The core idea centers around the fact the Task Scheduler "does not validate mount points before it deletes the corresponding `.job` file from the `C:\Windows\Tasks`", and this directory being writeable by a standard user. Furthermore, it uses a hidden file, `SA.DAT`, to prevent the user from converting the directory to a junction. As such, **a user can abuse an on-boot delete primitive to delete `SA.DAT` and privesc.** The post then talks about the d**ifficulties the team has had with vendors in reporting several of these privescs,** and why many of the bugs reported in the series remain unpatched 