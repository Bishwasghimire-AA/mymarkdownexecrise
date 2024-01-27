# H2 - Threat Modeling Summary and My Own Threat Model

## x) Read/watch and summarize

### My summary of [Threat modeling manifesto](https://www.threatmodelingmanifesto.org/)

Threat modeling is a process by which potential threats, such as structural vulnerabilities or the absence of appropriate safeguards, can be identified and enumerated, and countermeasures prioritized even before the system is build. TThe best use of threat modeling is to improve the security and privacy of a system through early and frequent analysis. Threat modeling is based on four key questions,
* What are we working on ?
* What can go wrong ?
* What are we going to do about it ?
* Did we do a good enough job ?

All these questions will be explained on the [following](https://github.com/bishwasghimire22/mymarkdownexecrise/blob/main/h2-shouldTerowearahelmet.md#summary-on-worlds-shortest-threat-modeling-course) summary

Threat modeling manifesto identifies two key guidelines, **values** and **principles**.

### Summary on [World's shortest threat modeling course](https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf) and [Threat modeling cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

* Threat modeling is done to anticipate problems when it's inexpensive to deal with them, before the system build where changes can be made quickly and easily.
* Key questions for threat modeling
  
  - What are we working on ?
    
      Its best to collabrate with people working on the project in different area(coding,networking etc.) and discuss on the model together and start making sketches or diagrams. It's good practice to record your documents as we are working on it, it will help identify what can go wrong. Although different techniques may be used in this first step of threat modeling, data flow diagrams (DFDs) are arguably the most common approach.
    
  - What can go wrong ?
    
     Afer the system is modeled We need to check all the vulnebrility in the system. Diffrent tools like STRIDE, kill-chain, etc. can be used as a guide to get answers. After possible threats have been identified, they must be ranked. Ranking should generally be based on the product of an identified threat's likelihood and its impact. A threat that is likely to occur and result in serious damage would be prioritized much higher than one that is unlikely to occur and would only have a moderate impact. All the answers we get should be paid equal attention. Basically, think like a bad person is going to think.
    
  - What are we going to do about it ?

   After having the knowledge of both system and threats, each threat identified earlier must have a response. Threat responses are similar, but not identical, to risk responses. [Adam Shostack](https://shostack.org/resources/threat-modeling) lists the following responses:

      - Mitigate: Take action to reduce the likelihood that the threat will materialize.
      - Eliminate: Simply remove the feature or component that is causing the threat.
      - Transfer: Shift responsibility to another entity such as the customer.
      - Accept: Do not mitigate, eliminate, or transfer the risk because none of the above options are acceptable given business requirements or constraints.

  - Did we do a good job ?
    
    The threat model must be reviewed by all stakeholders, not just the development or security teams. You need to validate your threat model by checking your work to make sure it’s as complete as possible.

## a) Security hygiene

* Security hygiene or cyber hygiene is a term that refers to best practices and other activities that computer system administrators and users can undertake to improve their cybersecurity while engaging in common online activities, such as web browsing, emailing, texting, etc.
* [Basic Practices](https://www.digitalguardian.com/blog/what-cyber-hygiene-definition-cyber-hygiene-benefits-best-practices-and-more) includes,
    -  Documenting all current equipmens and programs like hardware, software and applications in use
    -  Analyze the list of equipment and programs
    -  Create a common security hygiene policies and employ a cybersecurity framework 
* Some useful security hygiene practices I consider useful are
    - Enable multi-factor authentication
    - keeping software updated
    - practice safe browsing(HTTPS-enabled websites)
    - Back up important data
 
## b) Threat model

**Company Name: JJ Oy**

  JJ Oy is a company operating in the retail sector. Our main focus is to provide our customer with smooth and secure shoppping experience.  As a small business, trust and reputation are critical for success. The protection of customer information and secure online transactions is vital for maintaining customer trust and satisfaction.

  ### What are we working on ?
  
#### Our key assets

* Crown Jewel: Customer Personal Information (names, addresses, payment details): Critical due to privacy and regulations,
* Financial Transactions Data: Credit card details, Billing informations etc.
* E-commerce Platform and Website: Needed for continuity
* Inventory Management System: Essential for product availability
* Supply chain Information: Needed for maintaining buisness relationship
* Employee Information

#### Prioritization

* Crown Jewel: Customer Personal Information, Payment Information
* High: Product Inventory and Pricing Information, Website and E-commerce Platform
* Medium: Customer Service Database, Supply Chain Information
* Low: Employee Information





### What can go wrong ?

Applying the STRIDE model, potential threats include Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege.

* Unauthorized access to customer personal information leading to privacy breaches.
* Tampering with the e-commerce platform, affecting product listings or pricing.
* Employees repudiating actions, such as denying responsibility for unauthorized access.
* Disclosure of sensitive supplier information impacting business relationships.
* Potential denial-of-service attacks affecting the availability of the online shopping platform.

### What are we going to do about it ?

#### Risk Mitigation Strategies

* Implement multi-factor authentication and encryption for customer data.
* Regularly update and patch the e-commerce platform to address vulnerabilities.
* Establish robust employee training programs to minimize the risk of insider threats.
* Implement secure communication channels with suppliers to protect sensitive information.
* Utilize content delivery networks and DDoS mitigation services to mitigate the impact of denial-of-service attacks.


#### Risk Management Approach

* Reduce attack surface through regular security assessments and penetration testing.
* Limit entry points through secure coding practices and regular vulnerability assessments.
* Transfer risk through cyber insurance to cover potential financial losses.
* Accept certain risks that are deemed low-impact and have effective response plans in place.

### Did we do a good enough job ?

#### Continuous Evaluation

* Regular security audits and penetration testing to identify and address vulnerabilities.
* Continuous threat modeling to adapt to evolving threats and adjust mitigation strategies.
* Employee awareness programs to ensure ongoing adherence to security best practices.


#### Feedback Loop

* Regular review of incident response plans to incorporate lessons learned from real-world incidents.
* Collaboration with industry peers and information sharing to stay updated on emerging threats.










   I have use [Microsoft Threat Modeling Tool](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool) for this taskand if you like you can directly [download](https://aka.ms/threatmodelingtool) and try.

  
  

     
      
    
  
