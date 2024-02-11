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

Steps to send and recieve encrypted message  will require trust between both sender and reciever. This is done by setting a key pair of own and sharing the public key. Help for this task was recieved from [PGP - Send Encrypted and Signed Message - gpg](https://terokarvinen.com/2023/pgp-encrypt-sign-verify/?fromSearch=gpg). This task is done mainly using  Linux Terminal.

First I create a key pair for myself using the following command

    gpg --full-generate-key

It gave me a keypair, which consists of both my private(secret) key and public key. We will share the public key to anyone who wants to send us a message.

    pub   rsa3072 2024-02-07 [SC] [expires: 2026-02-06]
      5603147D7F1F0202B15B17C41B16F747A698FC67
    uid                      bishwas <bishwas@example.com>
    sub   rsa3072 2024-02-07 [E] [expires: 2026-02-06]

Next we export this public key, So we can exchange with someone who wants to send us an messages, in this case _Alice_. We can export the keys by following command.

    $ gpg --export --armor --output bishwas.pub

Using this commnad we save our file as "bishwas.pub" in hour home directory

Next we simulate _Alice_ for sending the message. We do this by using a folder to simulate Alice as different user in differnt OS or different computer. First we create a folder named Alice in our home directory and we change the mode of the folder to be only used by us as the owner.

    $ mkdir alice/
    $ chmod og-rwx alice/

Above command let us to create a working folder ALice in our home directory and give us permission to read,write and execute this folder. Form now this folder be used as a different user. To simulate Alice, we can just work inside this folder, and replace 'gpg' with 'gpg --homedir .' This way, Alice has her own settings and own keyring, separate from the one we actually use. Next we run the 'gpg' command to create alice configuration files.

    $ gpg --homedir . --fingerprint
    gpg: keybox '/home/bishwasg/alice/pubring.kbx' created
    gpg: /home/bishwasg/alice/trustdb.gpg: trustdb created

NOTE: Every command we run as Alice must start with 'gpg --homedir .'

Next we create Alice's keypair as we created our own.

    $ gpg --homedir . --gen-key

This gives us a key pair for Alice

    pub   rsa3072 2024-02-11 [SC] [expires: 2026-02-10]
      627E2AA5DC1D5646D1D0F08546054FBB63095792
    uid                      alice <alice@test.com>
    sub   rsa3072 2024-02-11 [E] [expires: 2026-02-10]

Next Alice imports the  public key of bishwas named 'bishwas.pub', which we had exported earlier in our home directory. First we copy the file 'bishwas.pub' to Alice folder and then alice imports the key in her own directory.

    cp -v bishwas.pub alice/
    'bishwas.pub' -> 'alice/bishwas.pub'

    gpg --homedir . --import bishwas.pub 
    gpg: key 1B16F747A698FC67: public key "bishwas <bishwas@example.com>" imported
    gpg: Total number processed: 1
    gpg:               imported: 1

Alice can check the fingerprint to verify that this is indeed bishwas's key. This step is needed if Tero's public key was obtained over insecure channel, like unencrypted email, a web page or a key server.

    pub   rsa3072 2024-02-11 [SC] [expires: 2026-02-10]
      627E 2AA5 DC1D 5646 D1D0  F085 4605 4FBB 6309 5792
    uid           [ultimate] alice <alice@test.com>
    sub   rsa3072 2024-02-11 [E] [expires: 2026-02-10]

    pub   rsa3072 2024-02-07 [SC] [expires: 2026-02-06]
      5603 147D 7F1F 0202 B15B  17C4 1B16 F747 A698 FC67
    uid           [ unknown] bishwas <bishwas@example.com>
    sub   rsa3072 2024-02-07 [E] [expires: 2026-02-06]

Here we can see all the public key that Alice holds, which can be used to send the encrypted message to the public key holder. Next ALice signs bishwas key to mark it as trusted, which can be done using the publick key or email address.

      gpg --homedir . --sign-key bishwas@example.com 

    pub  rsa3072/1B16F747A698FC67
     created: 2024-02-07  expires: 2026-02-06  usage: SC  
     trust: unknown       validity: unknown
    sub  rsa3072/0570CD4ED29F4FDB
     created: 2024-02-07  expires: 2026-02-06  usage: E   
    [ unknown] (1). bishwas <bishwas@example.com>


    pub  rsa3072/1B16F747A698FC67
     created: 2024-02-07  expires: 2026-02-06  usage: SC  
     trust: unknown       validity: unknown
     Primary key fingerprint: 5603 147D 7F1F 0202 B15B  17C4 1B16 F747 A698 FC67

     bishwas <bishwas@example.com>

    This key is due to expire on 2026-02-06.
    Are you sure that you want to sign this key with your
    key "alice <alice@test.com>" (46054FBB63095792)

    Really sign? (y/N) y

We can check the trust by.

    $ gpg --homedir . --fingerprint
    gpg: checking the trustdb
    gpg: marginals needed: 3  completes needed: 1  trust model: pgp
    gpg: depth: 0  valid:   1  signed:   1  trust: 0-, 0q, 0n, 0m, 0f, 1u
    gpg: depth: 1  valid:   1  signed:   0  trust: 1-, 0q, 0n, 0m, 0f, 0u
    gpg: next trustdb check due at 2026-02-06
    /home/bishwasg/alice/pubring.kbx
    --------------------------------
    pub   rsa3072 2024-02-11 [SC] [expires: 2026-02-10]
      627E 2AA5 DC1D 5646 D1D0  F085 4605 4FBB 6309 5792
    uid           [ultimate] alice <alice@test.com>
    sub   rsa3072 2024-02-11 [E] [expires: 2026-02-10]

    pub   rsa3072 2024-02-07 [SC] [expires: 2026-02-06]
      5603 147D 7F1F 0202 B15B  17C4 1B16 F747 A698 FC67
    uid           [  full  ] bishwas <bishwas@example.com>
    sub   rsa3072 2024-02-07 [E] [expires: 2026-02-06]

Using this trust Alice can now send encrypted message to bishwas. Bishwas also needs Alice's key to know that the message is really from Alice. The process is same as above, Importing alice's key, verifying and trusting the key. First we export alice's  key and copy in our home directory.cd

    $ gpg --homedir . --export --armor --output alice.pub
    cp -v alice/alice.pub .
    'alice/alice.pub' -> './alice.pub'

Next bishwas imports alice's keys and verifies it

    gpg --import alice.pub 
    gpg: key 46054FBB63095792: public key "alice <alice@test.com>" imported
    gpg: key 1B16F747A698FC67: "bishwas <bishwas@example.com>" 1 new signature

    gpg --sign-key alice@test.com

    gpg --fingerprint
    gpg: checking the trustdb
    gpg: marginals needed: 3  completes needed: 1  trust model: pgp
    gpg: depth: 0  valid:   1  signed:   1  trust: 0-, 0q, 0n, 0m, 0f, 1u
    gpg: depth: 1  valid:   1  signed:   0  trust: 1-, 0q, 0n, 0m, 0f, 0u
    gpg: next trustdb check due at 2026-02-06
    /home/bishwasg/.gnupg/pubring.kbx
    ---------------------------------
    pub   rsa3072 2024-02-07 [SC] [expires: 2026-02-06]
      5603 147D 7F1F 0202 B15B  17C4 1B16 F747 A698 FC67
    uid           [ultimate] bishwas <bishwas@example.com>
    sub   rsa3072 2024-02-07 [E] [expires: 2026-02-06]

    pub   rsa3072 2024-02-11 [SC] [expires: 2026-02-10]
      627E 2AA5 DC1D 5646 D1D0  F085 4605 4FBB 6309 5792
    uid           [  full  ] alice <alice@test.com>
    sub   rsa3072 2024-02-11 [E] [expires: 2026-02-10]

Now the trust between bishwas and alice have established on both keyring. Next alice sends a encrypted message to bishwas
First create a message.

    $ nano message.txt

![Secret message](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/b117b1f9-ba4c-413d-b311-e855439ba268)


Next we encrypt and send the message and send to bishwas.

    $ gpg --homedir . -e -r bishwas@example.com -s -o encrypted.gpg -a message.txt 

Here,
  * -e is to encrypt the message
  * -r is the recipient bishwas@example.com
  * -s, we sign our message using alice secret key, So bishwas can use alices's public key to decrypt the message
  * -a, is armor command to to make the message printable
  * -o output the 'message.txt' file as 'encrypted.gpg' file

After the encryption of our original message.txt file to encrypted.gpg file. It looks as follow

![Encrypted_secret_message](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/4e575a5c-868a-435a-b36d-9fc80dfdcc5b)

Even Alice can't decrypt the message now. It's been encrypted with bishwas's public key. Only bishwas can open it, because only bishwas has bishwas's secret key. We can send this encrypted file over the internet to bishwas now, but we are using simulation here so we copy this file to our home directory from alice's folder.

     $ cp -v alice/encrypted.gpg .
    'alice/encrypted.gpg' -> './encrypted.gpg'

Once the message is in home directory of bishwas, he can decrypt the message using his secret key.

    $ gpg -d encrypted.gpg 

And now bishwas can read the secret message sent by alice.

![decrypted_message](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/7ba6cc61-d10f-4fb6-ba72-6d903d76a348)

Using this method we can send and recieve encrypted message with anyone in the internet using 'GPG'





    

    



    



    
 





    



  

  

  



## 0) Voluntary bonus: ETAOIN

Ciphertext to be cracked:

     HDMH'B TH. KWU'YI AWR WSSTOTMJJK M OWQINYIMLIY! MB KWU BII, BTGPJI BUNBHTHUHTWA OTPDIYB OMA NI NYWLIA RTHD SYIEUIAOK MAMJKBTB. BII KWU MH DHHP://HIYWLMYCTAIA.OWG

To carck this cipher I used the good old pen and paper. At first glance, I didn't even know what I was looking at and where to actually start from. The text are in english but none of the word are making any sense. But, then after spending few time going back and forth with the text, I start to notice something. The main KEY was the final pieces of text, "DHHP://HIYWLMYCTAIA.OWG". This looked like an website, so I assume DHHP must be HTTP and OWG can be either COM or ORG. I start to fill all the ciphered text with these key letters I figured out and everything start to makes sense. I had to make some guesses when I hit the dead end. And finally after a good 2 hours of head scratch and paper scratch I figured out the text. Here is my work in paper.
 ![Deciphering_ETAOIN_1](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/9b5d0b8b-0247-43e7-bb41-29447e998b6b)


The Deciphered text read,
    
    THAT'S IT. YOU'RE NOW OFFICIALLY A CODEBREAKER! AS YOU SEE SIMPLE SUBSTITUTION CIPHERS CAN BE BROKEN WITH FREQUENCY ANALYSIS. SEE YOU AT HTTP://TEROKARVINEN.COM







