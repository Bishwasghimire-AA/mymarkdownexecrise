# Hashcat

## x) Summary of [Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02)

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

[Hashcat](https://hashcat.net/wiki/doku.php?id=hashcat) is the world’s fastest and most advanced password recovery tool. In this task we will Install hashcat in our debian OS in our Virtualbox. Some Linux distros have hashcat pre-installed in it. Our debian OS doesnot have hashcat preinstalled so we need to install the hashcat first. I have used [Cracking Passwords with Hashcat](https://terokarvinen.com/2022/cracking-passwords-with-hashcat/) and [How to use Hashcat Tutorial 2024](https://www.youtube.com/watch?v=5fy6Lq1vgZk&t=553s) for help with this task. You can install the hashcat by following command.

    sudo apt-get -y install hashid hashcat wget

After the installation we create a working directory for our work. I create a folder in my desktop called 'hashed'. you can create by folllowing command. 

    cd Desktop/
    ~/Desktop$ mkdir hashed
    $ cd hashed/
    
Now we will be inside our working directory. First thing we need now is the list of word dictionary from the internet or you can create your own too. For this exercise we will download a dictionary from the internet. I downloaded the [Rockyou](https://github.com/danielmiessler/SecLists/blob/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz) text file in my working directory. This dictionary consists of more than 14 million words text that have been known to be used as common password. We download the .tar.gz file which is a compressed file and we will decompress using tar command as follow.

    $ wget https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz
    $ tar xf rockyou.txt.tar.gz

![Download_rockyou_txt](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/e9cd8525-aa35-48d5-900d-0505fe9db033)

Now we have the rockyou.txt file in our working directory. Next we will crack this '8eb8e307a6d649bc7fb51443a06a216f'. In order to crack the hash we need to identify the hash types. It can be done in the terminal or by going to the [Hash Analyzer](https://www.tunnelsup.com/hash-analyzer/) website and check your hash type. Most common hash type are MD(MD2, MD4, MD5). The command to check the hash type is as follow.

    $ hashid -m 8eb8e307a6d649bc7fb51443a06a216f
    
![hashtype_search](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/882579c0-d34f-488e-906e-225e9b0b1d6e)

This command gives us possible hash types. Often, the right type is among top three candidates. If not, you can rule out many candidates based on where the hash was obtained (Windows, Linux...).

Let's try with md5, as it's a very common hash compared to md2 and md4.

Also you can type the following command in your terminal to get all the commands and help with using hashcat.
       
    $ hashcat --help

Above command gives you all the list of hashcat commands including the hashes code and much more

![Hashcat_help](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/2e151f9e-5264-4841-8a62-5f31f0de7f63)

Lets crack the hash '8eb8e307a6d649bc7fb51443a06a216f', it can be cracked with the following command

    $ hashcat -m 0 '8eb8e307a6d649bc7fb51443a06a216f' rockyou.txt -o solved  

This command means

* hashcat : 	the hash cracking program we just installed
* -m 0 :	type of the hash, the number we obtained from 'hashid' serach above
* '8eb8e307a6d649bc7fb51443a06a216f' : the hash we want to crack. Put single quotes around it, as many hashes contain special characters.
* rockyou.txt : Tells where to look for the reference word dictionary files
* -o solved : save the solution as plain text to a new file "solved" in working directory

The result is follow.

![cracked](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/2bb9ff1f-7b10-4fd8-a085-8664ed22f4ec)

Now we have cracked he password and its saved in our 'solved' file. We can read the content in our file by following command.

      /Desktop/hashed$ cat solved 
      8eb8e307a6d649bc7fb51443a06a216f:february

So the password is February.
    
![password is](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/9c773593-c442-4efc-9456-b2daac9cdb4a)

Cracking the password took about 5 seconds but if you have large database then it might take more time since our OS is a virtual machine. Just run it on your host OS, on real hardware and not a virtual machine. It will automatically detect your display adapter (GPU) and use that for a huge speed boost.


## c) Choosing a password manager

Here is the shortlist of some password managers of my choice,

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
* Also available as Mobile application in PlayStore or Google play store.

Next, you can can create a personal account to [sign up](https://vault.bitwarden.com/#/register?layout=default) for bitwarden app. NOTE: Other plans are going to cost you some money for subscription. After creating your account you are ready to use the Bitwarden as your password manager.

For this demonstration I choose the [Laksu](https://app.terokarvinen.com/) website. When you try to login using your credentials to the website you will be asked to confirm weather you want Bitwarden to save the password or not. 

![LAksu_login](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/b7cdc2d5-987b-4d34-a925-473ebb98f691)

In my case I choose to save my password in the "TEST" folder I created earlier. You can create different folders beforehand in the Bitwarden app as per your needs to save the passwords.

![Saving_password_Bitwarden](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/30895a38-3608-42e9-a945-fddf45518ad3)

This saved password will be used next time you try to login to your website. Also, if you forget your password, you can go to your Bitwarden app and view your password there.

![Bitwarden_dash](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/2eca2318-00ae-4e74-803e-820b88a92177)

You can also save your bank card details, Ids and confidential notes in the Bitwarden app. As mentioned earlier, all the password and documents are end-to-end encrypted(asymmentric encryption), meaning only way to decrypt the passwords is by providing our log in credentials for the Bitwarden app. So, only your Password for the Bitwarden app is going to unlock the saved password in a plain-text for you to read otherwise its all encrypted using hashes which isn't understandable to normal people. Therefore, only password you will need to remember is your Bitwarden app login password from now on.

Using Bitwarden you can also check vulnerability of your passwords. Bitwarden will also notify you if passwords like yours have been exposed by hackers in previous data breaches or not.

![exposed_password](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/bc925113-898c-4399-add4-a9d015441af1)

![Not_exposed](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/f7d46049-b5c7-4b02-b4ee-2f0a324ef64b)

Finally, it's always a smart choice to set up a [Two-Factor Authentication(2FA)](https://bitwarden.com/help/setup-two-step-login/) for your Bitwarden app to increase the security and protection of your valuable password and data.


![2 step login](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/d0b4449b-6d5c-4841-a0fd-813c5ca71eb4)





