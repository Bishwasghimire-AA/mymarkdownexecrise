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

      - Mitigate. Take action to reduce the likelihood that the threat will materialize.
      - Eliminate: Simply remove the feature or component that is causing the threat.
      - Transfer. Shift responsibility to another entity such as the customer.
      - Accept. Do not mitigate, eliminate, or transfer the risk because none of the above options are acceptable given business requirements or constraints.

  - Did we do a good job ?
  
     This is done by asking questions if they are willing to recomend threat modeling with colleagues.


  
  

     
      
    
  
