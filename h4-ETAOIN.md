# Encryption and Cryptography

## x)Summary on Applied Cryptography: [Chapter 1: Foundation](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001)

### TERMINOLOGY

* Messages are plaintext, encryption disguises messages (plaintext) into ciphertext. Decryption is the process of converting ciphertext back to plaintext.

* Authentication: Verifying the origin of a message. Integrity: Ensuring a message has not been modified during transmission. Nonrepudiation: Preventing a sender from denying they sent a message.

### Algorithms and Keys

* Cryptography Algorithm (Cipher) is a mathematical function for encryption and decryption. While restricted Algorithms is not suitable for modern use due to secrecy, lack of standardization, and security issues. Symmetric Algorithms uses the same key for encryption and decryption.

* Public-Key Algorithms(also called asymmetric algorithms) use different keys for encryption and decryption, known as public and private keys.

### Cryptoanalysis

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

### Security of Algorithms
  
*   Security depends on the difficulty/cost to break the algorithm.  If the amount of data encrypted with a single key is less than the amount of data necessary to break the algorithm, then you're probably safe.

*   Cryptography focuses on computationally secure (strong) algorithms. Algorithm is secure if it cannot be broken with available resources (current or future).

*   You can measure the complexity of an attack in different ways:
  
  * Data complexity: Amount of data needed for the attack.
  * Processing complexity: Time needed for the attack (work factor).
  * Storage requirements: Amount of memory needed for the attack.
  * Complexity of an attack is the minimum of these factors.
*  Good cryptosystems are designed to be infeasible to break with the computing power that is expected to evolve many years in the future.

### STEGANOGRAPHY

* Steganography is a method of concealing secret messages within innocuous messages. Historical methods include, invisible inks, pin punctures, differences in characters, grilles, etc.

* Modern Steganography method includes hiding messages in graphic images by replacing least significant bit of each byte, where the image remains mostly unchanged.

### SUBSTITUTION CIPHERS AND TRANSPOSITION CIPHERS

* Subtitution Cipher replace each character in the plaintext with a corresponding character in the ciphertext. While in Transposition Ciphers plaintext remains the same, but the order of characters is shuffled.

* Rotor machines are mechanical encryption devices introduced in the 1920s. eg. Enigma machine used by Germans in WWII.

### SIMPLE XOR

* Widely used in commercial software, particularly in MS-DOS and Macintosh environments.

* XOR encryption is not secure, easily broken, even without computers. XOR might offer basic protection but is not sufficient against determined cryptanalysis.

### ONE-TIME PADS

* One-Time Pad is a special case of a threshold scheme which involves a large nonrepeating set of truly random key letters. Each key letter is used only once, and used pad pages or tape sections are destroyed. Receiver has an identical pad and decrypts each letter of the ciphertext.

* Suitable for ultra-secure, low-bandwidth channels.
* Messages encrypted with one-time pads remain secure indefinitely against supercomputers and advanced technology.

* Perfectly secure if an eavesdropper can't access the one-time pad. Every plaintext message is equally possible, making cryptanalysis impossible.

* Suitable for short messages; impractical for high-speed communication channels.

### COMPUTER ALGORITHMS

* Most common algorithms are,
  * DES(Data Encryption Standard): Most popular computer encryption algorithm. It is a symmetric algorithm which uses the same key for encryption and decryption.
  * RSA (Rivest, Shamir, and Adleman): Named after its creators, is a popular public-key algorithms used for encryption and digital signatures.
  * DSA(Digital Signature Algorithm): Is also a public key algorithms which is used exclusively for digital signatures only.

### LARGE NUMBERS

* This part shows the probability of happening something, gathered from various sources.



## x)Summary of Prensentation Video by Disobey Youtube Channel

For this task I choose the Presentation title [[Disobey 2023] Hacks of the Future and The Role of Humans and Hackers - Connie McIntosh](https://www.youtube.com/watch?v=5WoZ9Pv9k0I&t=120s). On this presentation, Connie McIntosh, Head of Market Area Security at Ericsson, discussed the role of humans and hackers in the era of advanced AI technology, focusing on the potential risks and misuse of the popular language model, ChatGPT. The topic of her talk, which is about hackers, humans, and the chat API phenomenon, specifically focusing on the well-known chatbot AI, ChatGPT, from the perspective of a hacker. Here are the key points from the presentation,

* She mentions the use of chat GPT and similar AI models, which can write code in natural language, including malware, making it easier for attackers to create sophisticated attacks.
  
* She provides an example of modifying a code snippet to run in the background while opening a calculator app on a Windows computer. She then shares her past experience with using bad USBs (rubber ducky) to extract information and wonders if she can get a chat AI bot like ChatGPT to write a ducky script for her. She successfully manages to get ChatGPT to write a script that opens up a web browser and goes to her YouTube channel, and then takes it a step further by asking for a script that can show the Wi-Fi password of the computer and email it to her. Despite receiving a warning about content policy violations, she pushes boundaries and asks ChatGPT to write an additional script that will email the Wi-Fi password file to an additional email address.
  
* How even simple hacks, while sometimes requiring minimal technical knowledge, can still pose significant risks, specifically in regards to intellectual property (IP) code.
  
* Adversaries will pit AI machines against each other, integrate AI with hacking tools, create deepfake malware, and use AI for automated cyber reconnaissance and denial of service (DoS) attacks. Deepfake is emphasized as a significant threat, with examples like deepfake political videos and CEO voice authorization scams.
  
* Ransomware and phishing attacks are here to stay as long as humans use computers.
  
* Human error remains a dominant cause of security breaches. Upto 95% of cybersecurity breaches and privacy incidents are caused by humans unintentionally.
  
* Young adults aged 18 to 25 are more likely to fall for phishing scams than any other age group, making it crucial for organizations to identify and educate this demographic about cybersecurity.
  
* There is no way to truly limit AI as it has already been jailbroken, and the profitability of AI makes it unlikely that developers will turn it off. She suggests that regulation may be the only solution, but she doesn't believe it will happen soon enough.

## a)Encrypting and Decrypting a Message

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



## 0) Voluntary bonus: ETAOIN

Ciphertext to be cracked:

     HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG

To carck this cipher I used the good old pen and paper. At first glance, I didn't even know what I was looking at and where to actually start from. The text are in english but none of the word are making any sense. But, then after spending few time going back and forth with the text, I start to notice something. The main KEY was the final pieces of text, "DHHP://HIYWLMYCTAIA.OWG". This looked like an website, so I assume DHHP must be HTTP and OWG can be either COM or ORG. I start to fill all the ciphered text with these key letters I figured out and everything start to makes sense. I had to make some guesses when I hit the dead end. And finally after a good 2 hours of head scratch and paper scratch I figured out the text. Here is my work in paper.
 ![Deciphering_ETAOIN_1](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/9b5d0b8b-0247-43e7-bb41-29447e998b6b)


The Deciphered text read,
    
    THAT'S IT. YOU'RE NOW OFFICIALLY A CODEBREAKER! AS YOU SEE SIMPLE SUBSTITUTION CIPHERS CAN BE BROKEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROKARVINEN.COM







