# Encryption and Cryptography

## Summary on Applied Cryptography: [Chapter 1: Foundation](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001)

* Messages are plaintext, encryption disguises messages (plaintext) into ciphertext. Decryption is the process of converting ciphertext back to plaintext.

* Authentication: Verifying the origin of a message. Integrity: Ensuring a message has not been modified during transmission. Nonrepudiation: Preventing a sender from denying they sent a message.

* Cryptography Algorithm (Cipher) is a mathematical function for encryption and decryption. While restricted Algorithms is not suitable for modern use due to secrecy, lack of standardization, and security issues. Symmetric Algorithms uses the same key for encryption and decryption.

* Public-Key Algorithms(also called asymmetric algorithms) use different keys for encryption and decryption, known as public and private keys.

* Purpose of cryptography is to keep plaintext or key secret from eavesdroppers.
* Cryptoanalysis is the science of recovering plaintext without the key. It  may recover plaintext, key, or find weaknesses in the cryptosystem.

* Four genereal types of cryptoanalytic attacks:
  
  * Ciphertext-only attack: Where Cryptanalyst has ciphertext of several messages.
  * Known-plaintext attack: Where Cryptanalyst has ciphertext and corresponding plaintext.
  * Chosen-plaintext attack: Where Cryptanalyst chooses plaintext for encryption.
  * Adaptive-chosen-plaintext attack: A special case of chosen-plaintext attack with adaptive modifications.
    
* Common cryptoanalytic attacks are kown-plaintext attacks and chosen-plaintext attacks.
* Kerckhoffs's Assumption:  
    Secrecy should reside entirely in the key.
  
    Assumes cryptanalysts have complete details of cryptographic algorithm and implementation.  
    Emphasizes the importance of peer review for security evaluation.
    

## Summary of Prensentation Video by Disobey Youtube Channel

For this task I choose the Presentation title [[Disobey 2023] Hacks of the Future and The Role of Humans and Hackers - Connie McIntosh](https://www.youtube.com/watch?v=5WoZ9Pv9k0I&t=120s). On this presentation, Connie McIntosh, Head of Market Area Security at Ericsson, discussed the role of humans and hackers in the era of advanced AI technology, focusing on the potential risks and misuse of the popular language model, ChatGPT. The topic of her talk, which is about hackers, humans, and the chat API phenomenon, specifically focusing on the well-known chatbot AI, ChatGPT, from the perspective of a hacker. Here are the key points from the presentation,

* She mentions the use of chat GPT and similar AI models, which can write code in natural language, including malware, making it easier for attackers to create sophisticated attacks.
  
* She provides an example of modifying a code snippet to run in the background while opening a calculator app on a Windows computer. She then shares her past experience with using bad USBs (rubber ducky) to extract information and wonders if she can get a chat AI bot like ChatGPT to write a ducky script for her. She successfully manages to get ChatGPT to write a script that opens up a web browser and goes to her YouTube channel, and then takes it a step further by asking for a script that can show the Wi-Fi password of the computer and email it to her. Despite receiving a warning about content policy violations, she pushes boundaries and asks ChatGPT to write an additional script that will email the Wi-Fi password file to an additional email address.
  
* How even simple hacks, while sometimes requiring minimal technical knowledge, can still pose significant risks, specifically in regards to intellectual property (IP) code.
  
* Adversaries will pit AI machines against each other, integrate AI with hacking tools, create deepfake malware, and use AI for automated cyber reconnaissance and denial of service (DoS) attacks. Deepfake is emphasized as a significant threat, with examples like deepfake political videos and CEO voice authorization scams.
  
* Ransomware and phishing attacks are here to stay as long as humans use computers.
  
* Human error remains a dominant cause of security breaches. Upto 95% of cybersecurity breaches and privacy incidents are caused by humans unintentionally.
  
* Young adults aged 18 to 25 are more likely to fall for phishing scams than any other age group, making it crucial for organizations to identify and educate this demographic about cybersecurity.
  
* There is no way to truly limit AI as it has already been jailbroken, and the profitability of AI makes it unlikely that developers will turn it off. She suggests that regulation may be the only solution, but she doesn't believe it will happen soon enough.

## Encrypting and Decrypting a Message

For this task I choose to use [GNU Privacy Guard](https://www.gnupg.org/index.html), also known as GPG. It is an open source and free tool which allows us to encrypt and sign your data and communications. It uses a Asymmetric encryption, meaning it uses two set of keys, Private key and Public key. Public key can be used by the sender to send  an encrypted email to the person whom the key belongs, and the person uses his private key to decrypt the message.  It features a versatile key management system, along with access modules for all kinds of public key directories. GPG already comes installed in our debian OS.
![Gpg_version](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/e02941f3-22a0-4a53-bf1f-535376d21c59)

Steps to send and recieve encrypted message will will require trust for both sender and reciever. This is done by setting a key pair of own and sharing the public key. Help for this task was recieved from [PGP - Send Encrypted and Signed Message - gpg](https://terokarvinen.com/2023/pgp-encrypt-sign-verify/?fromSearch=gpg). This task is done mainly in a Linux Terminal.

First I create a key pair for myself using the following command

    gpg --full-generate-key

It gave me a keypair, which consists of both my private(secret) key and public key. We will share the public key to anyone who wants to send us a message.

    pub   rsa3072 2024-02-07 [SC] [expires: 2026-02-06]
      5603147D7F1F0202B15B17C41B16F747A698FC67
    uid                      bishwas <bishwas@example.com>
    sub   rsa3072 2024-02-07 [E] [expires: 2026-02-06]

Next we export this public key, So we can exchange with someone who wants to send us an messages, in this case _Alice_. We can export the keys by following command.

    







