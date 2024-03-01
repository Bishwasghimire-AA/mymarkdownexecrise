# The Dark Net

## x) Read and summarize

### [7 Things You Should Know About Tor](https://www.eff.org/deeplinks/2014/07/7-things-you-should-know-about-tor)

* Tor remains effective for anonymity despite NSA leaks and challenges.
* Tor is not exclusive to criminals; it serves diverse purposes for activists, military, families, and journalists.
* There is no military backdoor in Tor; it has been audited and confirmed by security professionals.
* No reported cases of US individuals being prosecuted for running Tor relays as of the article's knowledge cutoff.
* Tor is user-friendly, with the Tor Browser Bundle and Tails offering easy and secure usage.
* Ongoing efforts are made to improve Tor's speed by encouraging the creation of more relays.
* Tor is not foolproof; users can compromise their anonymity if used incorrectly, emphasizing the importance of proper usage and keeping software updated.

### Shavers & Bair 2016: [Hiding Behind the Keyboard: The Tor Browser](https://learning.oreilly.com/library/view/hiding-behind-the/9780128033524/XHTML/B9780128033401000021/B9780128033401000021.xhtml#s0010)

* Modified from Firefox, Tor ensures anonymous internet use by hiding users' IP addresses.
* Originally a government project, Tor is now an open-source platform, accepting global contributions.
* Balancing its role as a protector of anonymity and a potential enabler of illicit activities requires a nuanced approach from forensic analysts and investigators.
* Tor directs internet traffic through random relays with layered elliptic curve cryptography. Each relay removes a layer of encryption, making tracing nearly impossible. Exit relay connects to the user's target with an unencrypted connection.
* Tor network of relays is run by volunteers globally, making IP address investigations challenging.
* Tor browser, a modified Firefox, requires minimal technical skills for downloading and usage.
* Portable application, easy to install and configure in about 10 minutes.
* Tor's simplicity and strong anonymity make it appealing for legitimate and illicit use.
* Law enforcement may use Tor to avoid suspects detecting government IP addresses during investigations.
* FBI exploited a Firefox bug (CVE-2013-1690) to capture true IP addresses, MAC addresses, and Windows hostnames.
* Ongoing research explores attacking and disabling a large percentage of the Tor network to identify users.
* Internal corporate networks have an advantage in identifying Tor users.
* Network administrators can see Tor usage, aiding investigations if a suspect is identified within the corporate network.

## a) Install TOR browser 
I am using Debian "Bookworm" OS for this task. First you [Download](https://www.torproject.org/dist/torbrowser/13.0.10/tor-browser-linux-x86_64-13.0.10.tar.xz) the .tar file from the [Torproject](https://www.torproject.org/download/) website. It wil be downloaded in the Downloads directory. 

Next you can extract the .tar file from the GUI by right clicking the folder and selecting the option to archive the folder. Alternatively yo can run the following command in your terminal.

    Downloads$ tar xf tor-browser-linux-x86_64-13.0.10.tar.xz
    Downloads$ cd tor-browser/
    ~/Downloads/tor-browser$ ./start-tor-browser.desktop 

Above command starts the tor browser.

![Tor_front_page](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/0b27afa3-c5d7-4eb7-b9c2-8de5881f55a0)

    

## b) Browsing TOR network

The search engine I used is [Ahmia](https://ahmia.fi/]. This site's onion address is "http://juhanurmihxlp77nkq76byazcldy2hlmovfu2epvl5ankdibsot4csyd.onion/". On this website you can search for queries.


![Ahmia_search_page](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/78ced196-dd9a-4ae7-b8a2-7f6a2cce7a2c)

I searched for 'Forums' and I choose a forum called 'Darknet Army', whose onion address is,"http://dna777fdlbcv24cx5ctdvydvfa277vgb6wd6w4ztem6cho3kqogi7bqd.onion/". This forum is called hacking/carding forum. This forum has its own marketplace too where you can buy credit card details, malwares, software product keys, Hotel reservation and flight tickets too. Beside this people also seem to use the forum for some request such as passports, databases, muscle for hire as well. 

![Darknet_army](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/a78ea38e-39f6-4064-aff6-f0b4b01706f2)

I visited some marketplace in the dark web. I was particularly interested in the website called silkroad 4.0, whose onion address is  Silkroad is considered to be the oldest black market in the dark web since the time of [Dread Pirate Roberts](https://en.wikipedia.org/wiki/Ross_Ulbricht). You can find items like Drugs, stolen credit cards, weapons, fraud services, software and malware as well. All the transactions are done with Bitcoin (BTC) or Bitcoin Cash (BCH).


![Silkroad](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/e47ac5bc-20ab-46ec-a39c-14cd79032fa5)


Going through searches in https://ahmia.fi/ there are plenty of well known websites from leading Newsagency and govenment organisations. I even found US government spy agency called CIA in the darkweb whose onion address is, "http://ciadotgov4sjwlzihbbgxnqg3xiyrg7so2r2o3lt5wz5ypk4sxyjstad.onion/". I'm not sure if this is an official website from the government or not. The site have all the information on hiring process, forums and their own library. Just below is the picture of CIA's website in dark web and clear web with own DNS name.

![Dark_vs_clear_CIA](https://github.com/bishwasghimire22/mymarkdownexecrise/assets/144313610/fbae795a-4995-4771-8943-dda4977bb05c)
