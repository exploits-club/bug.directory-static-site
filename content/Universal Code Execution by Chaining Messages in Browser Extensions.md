tags: #browser_extension #browser
original link:  [Universal Code Execution by Chaining Messages in Browser Extensions](https://spaceraccoon.dev/universal-code-execution-browser-extensions/?ref=blog.exploits.club)
newsletter link: [exploits.club Weekly Newsletter 29](https://blog.exploits.club/exploits-club-weekly-newsletter-29/) 

---
## Exploits Club Summary:
> [@spaceraccoonsec](https://x.com/spaceraccoonsec?ref=blog.exploits.club) released a pretty fun write-up this week detailing his research in leveraging **vulnerable chrome extensions into RCE on the underlying host machines.** In some cases, browser extensions will allow communications with web pages via `postMessage`. Depending on if the extensions have been properly scoped or not, this could include result in **malicious sites exploiting logic bugs and breaking Same Origin Policy.** However, even more detrimental is **many extensions actually specify a binary on the host machine they want permission to interact with**. Think password managers needing access to the manager application on the host in order to autofill on the web. **As such, in some cases, malicious sites can actually interact directly with binaries on the host, resulting in RCE on the underlying machine. No V8 sandbox escape needed.**