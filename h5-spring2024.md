# Hashcat

## x) Sumarry of [Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02)

### [2.3 ONE-WAY FUNCTIONS](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003)

* A one-way function is a mathematical function that is easy to compute in one direction but significantly difficult to reverse.
* In cryptographic terms, given an input x, it is easy to compute the function f(x), but given f(x), it is computationally hard to find x.
* Although there is no mathematical proof of the existence of one-way functions, many functions behave like one-way functions, providing a foundation for cryptographic protocols.
* A trapdoor one-way function is a special type of one-way function that includes a secret trapdoor, which allows for reversing the computation under certain conditions.
* Easy to compute in one direction, hard to reverse but with knowledge of the secret (trapdoor), reversal becomes easy to compute.
* Trapdoor one-way function is used in public-key cryptography for secure communication.

### [2.4 ONE-WAY HASH FUNCTIONS](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec004)

* Also known as compression function, contraction function, message digest, fingerprint, cryptographic checksum, message integrity check (MIC), and manipulation detection code (MDC).
* These functions convert variable-length input (pre-image) into a fixed-length output (hash value), serving as a fingerprint for the pre-image.
* Should be collision-free: hard to generate two pre-images with the same hash value.
* Publicly known; security relies on one-wayness and the difficulty of generating a matching pre-image.
* A single bit change in the pre-image changes, on average, half of the bits in the hash value.
* Used in file verification to prevent unauthorized changes and also, recipients can verify the hash without the need for a key.
* Message Authentication Codes (MAC) is a one-way hash function with the addition of a secret key.
* MAC has similar theory to hash functions, but only someone with the key can verify the hash value.
* MAC cryptographic mechanism provides a layer of confidentiality, allowing parties with the secret key to authenticate the origin and integrity of the message or data.

## a) and b) Installing hashcat and cracking hash

## c) Choosing a password manager

Here is the shortlist of some parrword managers of my choice,

* [LastPass](https://www.lastpass.com/why-lastpass)
* [1Password](https://1password.com/product/features)
* [Bitwarden](https://bitwarden.com/about/)

My choice among these password manager is Bitwarden because,

* Bitwarden protects against password breaches, unauthorized access, and insecure password practices.
* Bitwarden offers strong security with end-to-end encryption, open-source transparency, and flexible hosting options.
* All data, including passwords, is end-to-end encrypted.
* Open source license with premium plans available, which encourage and promote community-driven security audits.
* Cloud-based storage, which is customizable, allowing users to choose Bitwarden's servers or self-hosting for added control.

## d) Demonstration of Bitwarden

* First [download](https://bitwarden.com/download/) and install the Bitwarden app for your desired Operating System, Supported Os are Windows, MacOs and Linux
* Also available as your web browser extension supported by popular browsers like Chrome, Safari, Firefox, Brave, Microsoft edge, Tor browser etc to name some.
* Also abilable as Mobile application in PlayStore or Google play store.

Next, you can can create a personal account to [sign up](https://vault.bitwarden.com/#/register?layout=default) for bitwarden app. NOTE: Other plans are going to cost you some money for subscription. After creating your account you are ready to use the Bitwarden as your password manager.

For this demonstration I choose the [Laksu](https://app.terokarvinen.com/) website. When you try to login using your credentials to the website you will be asked to confirm weather you want Bitwarden to save the password or not. 

![LAksu_login](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/b7cdc2d5-987b-4d34-a925-473ebb98f691)

In my case I choose to save my password in the "TEST" folder I created earlier. You can create different folders beforehand in the Bitwarden app as per your needs to save the passwords.

![Saving_password_Bitwarden](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/30895a38-3608-42e9-a945-fddf45518ad3)

This saved password will be used next time you try to login to your website. Also if you forget your password, now you can go to your Bitwarden app and view your password there.
![Bitwarden_dash](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/2eca2318-00ae-4e74-803e-820b88a92177)

You can also save your bank card details, Ids and confidential documents in the Bitwarden app. As already mentioned earlier all the password and documents are encrypted inside the app. So only your Password for the Bitwarden app is going to unlock the saved password in a plain-text for you to read otherwise its all encrypted using hashes which isn't understandable to normal people. Therefore, only password now you are going to need to remember is your Bitwarden app login password only.

Using Bitwarden you can also check vulnerability of your passwords. Bitwarden will tell you if passwords like yours have been exposed by hacker previously or not.

![exposed_password](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/bc925113-898c-4399-add4-a9d015441af1)

![Not_exposed](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/f7d46049-b5c7-4b02-b4ee-2f0a324ef64b)

Finally, it's a smart choice to set up a [Two-Factor Authentication(2FA)](https://bitwarden.com/help/setup-two-step-login/) for your Bitwarden app to increase the security and protection of your valuable password and data.


![2 step login](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/d0b4449b-6d5c-4841-a0fd-813c5ca71eb4)





