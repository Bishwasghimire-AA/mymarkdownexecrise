# Summary from [OWASP Top 10](https://owasp.org/Top10/) and [OWASP Webgoat](https://owasp.org/www-project-webgoat/)

[OWASP](https://owasp.org/about/)(Open Worldwide Application Security Project) is a nonprofit foundation that works to improve the security of software. The OWASP Top ten is a list of the ten most critical web application security risks. It provides an awareness and guidance to developers and security professionals on common vulnerabilities that can be exploited by attackers. This list is formed by contribution of people from different IT fields like Data scientists, web designer, Translators, Testing guide, and code review guide etc. and the Internet community surveys. I am going to summarize few catagories from the list below.

## x) Sumarry on [A03:2021-Injection](https://owasp.org/Top10/A03_2021-Injection/), [A05:2021-Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/), [A06:2021-Vulnerable and Outdated Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/)

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

## a) Installing Webgoat

I run webgoat in my browser using the Jar file from [Webgoat github](https://github.com/WebGoat/WebGoat/releases) repository and instruction from [Try Web Hacking on New Webgoat 2023.4](https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/). Here is my webgoat webpage running, alongside the CLI to run the jar file I downloaded earlier.
![Running_Webgoat](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/3a20f39e-2124-429f-8947-0081c47dfcba)

## b) Solving Webgoat 2023.4: General: Developer tools.

I completed this exercise using resources from [Cyber World Hindi](https://www.youtube.com/watch?v=S_vkbQId1as&list=PLSbrmTUy4daP4IAndCi5TsJeoDWpPxGc5&index=2)- Webgoat tutorials Videos. Please note it's in Hindi Language.

### HTTP Basics

In Developers tool(F12 or Ctrl+Shift+i), find the Network tab and attck2, and in the Headers tab you will see the Request method POST and under the Payload tab you will find the magic number, in my case the number was 91. I guess it might be different for other.


![HTTP_Basics_3_POST](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/37456cfc-d276-4057-b134-34a711ee05f7)


![HTTP_Basics_3_number](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/931a97b6-e645-45f8-82b1-3615f7be33ff)

### HTTP Proxies

 HTTP Proxies receive requests from a client and relay them. Proxies sit between your client and the server the client is talking to.

 ## d) [SQLZoo Tutorial](https://sqlzoo.net/wiki/SQL_Tutorial)

   ### 0 SELECT Basics

 This example uses WHERE clause, the query sting should be in a single quote.

 ![SELECT_basics_1](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/f062c7b9-7bf9-4b43-8e76-77d49368eb90)

 Second task uses the word IN which allows us to choose multiple items from the database.
 
![SELECT_basics_2](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/15035bbf-59c5-418c-a70f-6809c078dbab)

Third task uses the word BETWEEN to check the range of given data under provided condition. Here we use different keywords like, SELECT, FROM, WHERE, BETWEEN and AND 

 ![SELECT_basics_3](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/b80a39a1-9c04-4840-af3c-46538cf130ee)

 ### SELECT from WORLD

 For this task I submitted the query using >= to get the list of all the country with population of at least 200 million.

![SELECT_World_2](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/e5d10451-4033-4d35-a5cf-3173ff2140c1)

All the other task went forward easily so I only posted the ones that had given me multiple errors. I have used [Jess Chase](https://thedatasleuth.github.io/2018/08/11/SELECT-Basics.html) for help and reference for all the stuck levels.

