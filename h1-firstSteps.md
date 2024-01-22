# h1 Homework

## Summary on the podcast I listened

  For this task I choose [__Episode 53: Shadow Brokers__](https://darknetdiaries.com/episode/53/) to listen. I found this topic very interesting and here are the key topics I found interesting
  * Shadow brokers are the hacking group who claimed to have leak the NSA ANT catalouges
      - The catalouge was a collection of sophisticated hacking tools and technologies used by the Tailored Access Operations (TAO) division of the United States National Security Agency (NSA). "ANT" stands for Advanced Network Technology, and the catalog provides details about various hardware and software implants, exploits, and techniques employed by the NSA for cyber operations.
 * The leaks included vulnerabilities affecting various operating systems and network equipment, and they had significant implications for cybersecurity worldwide. Some of the exploits released by the Shadow Brokers were later used in high-profile cyber attacks, such as the WannaCry ransomware attack in 2017.
 * Shadow Brokers is credited with leaking the EternalBlue exploit. EternalBlue specifically targeted a vulnerability in Microsoft's Windows operating system.

   My questions from this podcasts are:
   * How has the global cybersecurity landscape evolved in response to the release of EternalBlue, and what measures have organizations taken to protect against similar exploits?
   * What were the motivations and identity of the Shadow Brokers? It might adds a layer of complexity to understanding the dynamics of cyber threats. Also, uncovering their motives may contribute to better defense strategies.


## My key summary on Intrusion Kill Chain and Course of Action

The intrusion kill chain is a concept used in cybersecurity to describe the various stages of a cyber attack, from the initial planning and reconnaissance to the final objective of the attacker. The idea is to break down the attack process into a series of distinct steps, each of which represents a phase in the overall attack lifecycle. By understanding and analyzing these stages, cybersecurity professionals can develop strategies and defenses to detect, prevent, and mitigate cyber threats.This is anintegrated, end-to-endprocess described as a “chain” because anyone deficiency will interrupt the entire process.

The typical stages of an intrusion kill chain include:

* Reconnaissance: In this phase, attackers gather information about the target, such as identifying potential vulnerabilities, system configurations, and potential targets.

+ Weaponization: This is where the attackers create or acquire the tools and malware needed to exploit the identified vulnerabilities.

- Delivery: Attackers deliver the malicious payload to the target system, often using methods like phishing emails, infected websites, or other means.

* Exploitation: The malicious payload is executed on the target system, taking advantage of the vulnerabilities identified in the reconnaissance phase.

* Installation: Once the payload has exploited the system, it installs itself or other components on the compromised system to establish a persistent presence.

* Command and Control (C2): The attackers establish communication channels with the compromised system to control and manage the ongoing attack.

* Actions on Objectives: This is the final phase where the attackers achieve their primary goals, which could include data theft, system manipulation, or disruption of services.

The term "course of action" in the context of cybersecurity generally refers to the steps or strategies taken by an organization or individual to address a security incident or mitigate potential risks. It involves planning and executing a set of actions to prevent, detect, respond to, and recover from security incidents. The specific course of action can vary depending on the nature of the threat, the organization's security posture, and the type of assets at risk. Here is a general outline of the course of action in cybersecurity,

* Detect: Indicates the action of identifying and recognizing a threat or activity.
* Deny: Involves preventing an adversary from accessing, using, or acquiring specific information or resources.
* Disrupt: Focuses on interfering with or interrupting the adversary's operations or communications.
* Degrade: Refers to reducing the quality or effectiveness of an adversary's capabilities.
* Deceive: Involves providing false or misleading information to mislead or confuse the adversary.
* Destroy: Entails eliminating or rendering useless the adversary's capabilities or resources.

## Installing Debian

Installed live debian using the Virtual Machiines. Host device is running on windows 11 OS. I ran into few problems during the installation
- First problem I ran into during the installation was the warning of "Please use a kernel appropirate for your CPU". Here is the Screenshot ![Fail_to_install_debian](https://github.com/Bishwasghimire-AA/mymarkdownexecrise/assets/144313610/053a88a7-27f3-4ce8-b289-5c84da0e3f5f)

  I fixed this problem manually by changing the debian file to 64-bit, and it worked
- Second problem was  with logging in after debian was installed. Even though I had provided the correct username and passwordd it kept on giving me warning for incorrect password. Here is the screenshot of the warning ![Incorrect_password_warning](https://github.com/Bishwasghimire-AA/mymarkdownexecrise/assets/144313610/0d12dd5c-8ff9-412f-a3a5-33f9278297ee)
  
  This problem got fixed after uninsatlling and reinstalling the debian about 3 times from my virtual machine.
- Finally I'm able to have my own Linux OS in my VM. I followed all the insatllation guide provided in Tero's [Website](https://terokarvinen.com/2021/install-debian-on-virtualbox/)

 And here's how my desktop works after the final tweaking.![my_debian](https://github.com/Bishwasghimire-AA/mymarkdownexecrise/assets/144313610/aba1e167-7aeb-4e5a-b6e9-5b8719d4a95a)

 ## Voluntary multi-week bonus( Set1 Challenge1 )

Having no previous knowledge of any CLI or any coding I tried to do this first task using help from [ChatGPT](https://chat.openai.com/c/5eba79d8-012a-4fb7-bdca-fbca8edb36ef). and this [Forum](https://superuser.com/questions/158142/how-can-i-convert-from-hex-to-base64/416630). I am very happy to see that I got the result wanted in the [Website](https://www.cryptopals.com/sets/1/challenges/1). Things I learned for this command were,
- echo Command:
  -echo is a command used to print text to the terminal.
- xxd Command:
  -xxd is a command-line utility that creates a hex dump of a given file or standard input.
  -The -r -p options tell xxd to reverse (convert from hex to binary) and use plain formatting (no additional information).
- base64 Command:
  -base64 is a command-line utility that encodes or decodes data in base64.
  -It takes the binary output from xxd (which was the reverse of the original hex string) and encodes it in base64.

  Here is my result ![set1_chlng1_cryptopal](https://github.com/Bishwasghimire-AA/mymarkdownexecrise/assets/144313610/6d65b4cd-0336-4a7d-93a9-c2916f73b8ad)
