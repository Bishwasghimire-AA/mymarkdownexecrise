# Summary from [OWASP Top 10](https://owasp.org/Top10/) and [OWASP Webgoat](https://owasp.org/www-project-webgoat/)

[OWASP](https://owasp.org/about/)(Open Worldwide Application Security Project) is a nonprofit foundation that works to improve the security of software. The OWASP Top ten is a list of the ten most critical web application security risks. It provides an awareness and guidance to developers and security professionals on common vulnerabilities that can be exploited by attackers. This list is formed by contribution of people from different IT fields like Data scientists, web designer, Translators, Testing guide, and code review guide etc. and the Internet community surveys. I am going to summarize few catagories from the list below.

## Sumarry on [A03:2021-Injection](https://owasp.org/Top10/A03_2021-Injection/), [A05:2021-Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/), [A06:2021-Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)

### A03:2021-Injection

* Dropped from first position on 2017 to third position on 2021
* Applications are vulnerable when user-supplied data is not properly validated, filtered, or sanitized
* Various injection types include SQL, NoSQL, OS command, Object Relational Mapping (ORM), LDAP, and Expression Language (EL) or Object Graph Navigation Library (OGNL) injection.
* Source code review is recommended for detecting injection vulnerabilities.
* Use LIMIT and other SQL controls within queries to prevent mass disclosure of records in the event of SQL injection.
* Developers should be educated about secure coding practices and the risks associated with injection vulnerabilities.

### A05:2021-Security Misconfiguration
* With more shifts into highly configurable software, this category moved up from sixth position in 2017 to fifth position in 2021
* Security misconfigurations refer to the improper implementation or setup of security controls in a system, application, or network, leaving vulnerabilities that can be exploited by attackers.
* Vulnerabilities may arise from missing security hardening, improperly configured permissions, unnecessary enabled features, default accounts/passwords, revealing error handling, disabled security features in upgraded systems, and insecure settings in various components.
* Implement secure installation processes with repeatable hardening procedures.
* Maintain a minimal platform without unnecessary features and components.
* Regularly review and update configurations following security notes, updates, and patches.

### A06:2021-Vulnerable and Outdated Components

* Organizations may be vulnerable if they are unaware of the versions of all components, both client-side and server-side, including direct use and nested dependencies.
* Vulnerabilities arise when software, including OS, servers, databases, applications, and libraries, is outdated, unsupported, or vulnerable.
* Lack of security in the configurations of components, as outlined in A05:2021-Security Misconfiguration, contributes to the vulnerability landscape.
* Establish a robust patch management process to remove unused dependencies, unnecessary features, components, files, and documentation.
* Regularly monitor for libraries and components that are unmaintained or lack security patches for older versions.
* Establish an ongoing plan for monitoring, triaging, and applying updates or configuration changes throughout the application or portfolio's lifetime.

## Installing Webgoat

I run webgoat in my browser using the Jar file from [Webgoat github](https://github.com/WebGoat/WebGoat/releases) repository and instruction from [Try Web Hacking on New Webgoat 2023.4](https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/). Here is my webgoat webpage running, alongside the CLI to run the jar file I downloaded earlier.
![Running_Webgoat](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/3a20f39e-2124-429f-8947-0081c47dfcba)


