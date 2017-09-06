# A Citizen's Guide to Digital Freedoms

# Background

## What and Why
The goal of this guide is to help technical and non-technical people alike,
particularly political and social activists, keep their information and
communications confidential.

## Help Needed

1. Technical people: We welcome contributions, additions and corrections.
1. Non-technical people: Information about what areas are unclear or in need of
   improvement is hugely valuable.

Non-technical people: To contribute you can simply comment on github.

Technical people: First "clone" the repository on github, modify it as desired and then comment
with a "pull" request. Sadly, gist lacks an explicit "pull request" feature,
this is the closest we can get.

## Ownership and Distribution

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), though we'd prefer that you just submit patches to [this gist](https://gist.github.com/bluehat/76a07a5d25f038a89f3b99c54a9a94a9). If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate). All Amazon links include the EFF referral tag, so they get money.

This information is kept in git format because it is easy to transmit git repos peer-to-peer. You are encouraged to download a copy. Suggestions on how to keep the guide trustworthy and from having merge issues in a peer-to-peer environment are appreciated. 

# Terminology
## Security
Security is a very nebulous term, including concepts like financial security, so
for our purposes we're going to stick to 2 particular types of security.

1. Device Security: The inability for anyone to use or modify the software on a device you own, without your authorization.
1. Communication security: The security of your communications with another person, to clarify what that means we break that down further below.

It's tempting to call things "secure" or "insecure" and you hear these terms used all the time by media and even by techies. Don't listen to it. In reality security is *always* a gradiant. Something with all the best technology done the best way anyone knows may have a tiny flaw that no-one noticed.

A burgler breaks in to a house via the easiest method. A lock on the window doesn't help if the door is literally left wide open. Alternatively, A solid steel door with a fancy lock doesn't help if it's next to a glass window trivially broken. Similarly we measure a technology's security by it's *weakest* point, not it's
strongest.

Continuing the analogy most burglers don't come with ladders. There may be a use in using a steel door, even if the upper story windows are unlocked. For this reason we can't just talk about security as a single slider. It depends on who you are trying to keep things secure *from*.

This is all important because it's tempting to say "Ugh, everything is insecure". While that's true in a sense, we still lock our doors even though a burgler could use a wrecking ball. Even when we're talking about governments, dramatic measures get expensive, and often give away information a government doesn't want people to know (like that they just smashed up your house).  

Unfortunately, all this means we can't just say "Do this, it's secure", "don't do this, it's not secure". We have to explain the tradeoffs. So, while we try and keep the explanations as simple as possible, we try and do so without washing out these important details.

## Communication Security
Communication security is made up of 3 components.

1. Encryption: The inability for someone besides the person you are communicating with who sees your communocation to understand it.
1. Authentication: The assurance that you are communicationg with the person you think you are.
1. Anonymity: The assurance that no-one can tell who you are, or who you are talking to.

It should be noted that the 3'rd bullet here, though highly desirable, is rarely acheivable, so in regular conversation the combination of 1 and 2 are usually considered "sufficient". For this document we'll try and spell out exactly what we mean rather than just calling something "secure" overall.

## Encryption
We should talk about encryption in a little more detail. 

Not all encryption is created equal and just because something is "encrypted"
doesn't mean it can never be read by anyone. As a simple example, if I use
"rot13" to encrypted my email... that is I take ever letter and change it to the
letter 13 letters further through the alphabet (wrapping around if I run out of
letters)... while technically encryption, many children could "crack" this and
read the original message.

In practice encryption methods suffer from 2 classes of problem
1. All can be "cracked" (read by someone besides the person who you intend to read it) with sufficient computational power. As computers get faster, that computational power gets easier to get a hold of. While some encryption may take an amount of computational power functionall impossible to get, most do not, and many older technologies can already be cracked by say... China if they care enough to spend a couple billion on cracking it (say, with 2 days time on their biggest computer).
1. Most encryption technologies don't have any strong theoretical backing. It's often the case that mathematical tricks can significantly reduce the computational power needed. As new computational tricks are discovered

Why are we bringing this up? Because, it's important to realize that no matter what you do, if your conversation is "logged" (stored somewhere) by someone, even if it's encrypted so they can't read it now, some day they may be able to read it. The cost to do so will also constantly drop as computers get faster.

We'll try and address how *good* a technology's encryption is. Good generally means "probably won't be easy to read within your lifetime".

## Logging
Logging technical terminology for the simple act of storing information. Almost every system in the technical world is constantly logging. It's pretty obvious why you might care about logging if you are worried about confidental information and communications. So, here are a few things that are logged, for you to keep in mind: 

Here's some you probably know about
1. The location of all cell phones in the U.S.
1. [The calling and called phone numbers of every phone call made in the U.S.](https://www.theguardian.com/business/2016/oct/25/att-secretly-sells-customer-data-law-enforcement-hemisphere).
1. Most websites log the "internet address" of every machine that accesses them. They also usually log all major or interesting operations.

Here's some you probably don't
1. All international phone conversations, with full text, and many domestic ones
1. Virtually every email, foreign and domestic, which flows over the public internet (so, most of them)

## Monitoring 
A lot of information also isn't logged, but is monitored in real time. You should assume that every bit of information that flows over the internet is being monitored in real time by the U.S. NSA... While not strictly true, it's very close to true.

This means that any information which flows over the internet that is not encrypted, will be analyzed.

Stuff deemed "interesting" is *also* logged. This may include all traffic between certain "suspicious" computers.

## Exploit
This is flaw in a piece of software or hardware, combined with a way to
"exploit" that flaw to violate the security of a system (whether a device or
communication system).

## Zero Day Exploit
Often shortened to simple "Zero Day"  This is an "exploit" that has never been used before. That's important because it means the designers of the system don't have any way to know about the flaw, and thus most likely neither do you.

## Patch 
A fix for an "exploit". To say that an exploit has been "patched" means that it's been fixed. When you download and install a "patch", or an update containing a patch, you are applying fix to your system.

This terminology seems esoteric, but patching is VERY important. 

If you use good software and hardware, it will usually be fixed pretty fast once the designers find out there's a flaw. Zero day exploits are worth a LOT of money, so neither hackers nor governments want to use them if they don't have to. Instead, they'll use already known exploits taking advantage of the fact that users often don't actually install the patches. 

As a result, most real world security breaches use exploits that have already been patched. Just keeping up with patches (system updates) will put you far ahead of the game. We'll talk about this more in "Device Security".

## Attacker
An attacker refers to a person trying to get your confidental information. That
is, they are trying to violate the security of some system that has the
information.

We're going to use this term a lot. In our analogy earlier, we noted that most
burglers don't bring ladder. It's important to understand who wants your
confidental data, so you can understand what tools they have at their
disposal... do they have a ladder?

## State Actor or "APT"
This is a specific category of "attacker". Once you're listening for it you'll hear this term pop up in the media a lot. "APT" stands for "Advanced Persistant Threat" and is usually assumed to be synonymous with "a country" (though it's not actually). Thus the other term "State Actor". The critical factor that makes an attacker an APT is that they have a LOT of resources to throw at trying to get confidential information. A country can subpeana corporations and make them hand over info, physically threaten people, pay millions for black market zero day exploits, build enormous multi-billion dollar computers just for cracking encryption, etc.

If you are a loud political disidant trying to keep the U.S. government from getting your confidential information, you're dealing with a state actor. As an example, lets say you're organizing a protest group. While they will likely happily ask the phone company for a log of your location, log all your cellphone calls, spend a couple of physical people to covertly follow you around and see who you talk to in person, etc. You may still not be worth burning a zero day exploit on, or several days of a billion dollar datacenter to crack even poor cryptography. In short... a state actor probably has the "ladder" to reach your second story window. Keeping them out is going to be a bit harder.

Just because they have a ladder or wrecking ball though, doesn't mean they're willing to use it. When your opponent is in to the APT category, while the attacker has many resources, they have other priorities to spend them on and use of those tools may cause political problems. Keep that burgler in mind, what's the easiest path to your confidential information? Don't forget about options like declaring you a terrorist and arresting you. If that's politically feasible, it may be the open door next to the carefully locked window of your technology. 

For these reasons, even in the case of a state actor, there are likely to be limits to what they can or will do, and thus there's hope in making your data "secure enough".

## Malware/Spyware/Trojan
Malware is any software designed to violate the security of your device.

Spyware refers specifically to software designed to watch what you do, like watching what you type on your keyboard, and usually send that information over the internet to an attacker.

A Trojan is a piece of software designed to allow an attacker to control your device remotely.

So spyware and Trojan's are specific types of malware.

# Device Security
We've defined device security, lets talk about why we care. If the attacker has direct access to your device, communications using that device aren't going to be secure. All the encryption and authentication aren't going to help if someone can literally see what you are typing in the first place.

So, how do you keep a device secure?
1. The #1 thing you can do to keep your device secure is to keep the software up to date. Remember the section on patching? Do it.
1. Don't give your attacker physical access. All devices can be compromised given physical access, without exception, and usually in a way that would be nearly impossible to detect. Examples include keyloggers under the keyboard of a laptop, or in a replacement cellphone screen; firmware modifications to various hardware; Modifications of operating systems or applications; and the list goes on. 
1. Install only a minimum of software you need, and get it from reputable places if you can. Any software you install could be malware. Software from an app-store is less likely to be a problem, as the corporation running the store is looking for them, but sometimes some slip by. Software you get from an email, or from a website an email pointed you to is very likely to be malware, even if it *looks* like a friend sent the email. We'll talk about email later on.

Some systems are known to have extant exploits, or even be "pre" crompromized from the factory, and aren't getting fixed for one reason or another, so here's a partial list of stuff you may want to avoid, and some alternatives.

You may notice a lot of cellphone issues are on this list. This is partly because of the nature of FCC regulations and closed specs of cellphone chips...  but it's also because everyone uses a cellphone these days, and so governments have a huge incentive to figure out how to get information from them. It's useful to keep in mind that it's far more useful to build exploits for commonly used systems for exactly this reason. Less used systems are less targetted, because the work is the same for less gain. 

## Known Compromised Systems
### Windows 10
[Windows 10's EULA stipulates that everything you do on your computer will be logged by Microsoft, and that these logs will be available to the government.](http://www.newsweek.com/windows-10-recording-users-every-move-358952).

Windows is what most laptops you might purchase would come with, so this basically means nearly all factory laptops. Don't worry though, there's some reasonable work-arounds.

Risks:
1. Everything you do may be logged, and that log may be subpeana'd (or just
   requested) by a government, or lost to a hacker who infiltrates microsoft.

Alternatives:
1. Apple computers are one option, though they are quite expensive, and you're still trusting just a single company. On the other hand, some company had to build the hardware, and you have to trust them anyway.
1. Some laptops can be had with Linux pre-installed. These are usually more than their windows competitors, but may be cheaper than Apple machines. Linux is not made by a single company, and many experts read and modify it looking for security flaws. On the other hand, this does give government agencies an opportunity to add security flaws.
1. Buy a normal laptop, and install Linux on it for free.

Obviously installing Linux is a bit of complex affair, and likely requires a technical person. That said, it's no harder to use once installed than Windows or OS-X, and most software you'd want to use on it is free... Having a friend help you out may be a good option.

### Lenovo Laptops with Windows

Lenovo laptops have a [history of manufacturer-bundled malware](http://www.theregister.co.uk/2015/08/12/lenovo_firmware_nasty/) which opens a security vulnerability on the system if the system boots Windows. The code is injected before Windows launches. It is considered a malware and it is baked into the physical boards they ship you. This practice has gone on for multiple years, and has caused some [US federal government branches to try to not use the systems anymore](http://www.wsj.com/articles/u-s-navy-looks-to-replace-ibm-servers-for-security-after-lenovo-purchase-1432047582). [Obama has required that several federal agencies get approval for any systems they purchase if the systems are made in China](http://www.reuters.com/article/us-usa-cybersecurity-espionage-idUSBRE92Q18O20130328), supposedly for this reason. 

Risks:
1. The malware adds a major security flaw to of what would otherwise be secure webbrowsing. This means an attacker may have easy access to modify what you see of the web, including what software you download... functionally compromising the entire device. 

Alternatives:
1. Install Linux on a Lenovo laptop, or buy a machine made by any other company.

### Cellphones, U.S. 911 support

All cellphones sold in the U.S. are required by law to have 911 support. Ostensibly this is a suite of features allowing a caller to call 911 on any phone without unlocking the phone, having a cell plan, etc. and allows the 911 operator to locate the phone when such a call is made. Most phones sold outside the U.S. are still legal for sale here, and thus still include this feature.

The features that allows this though also allow the phone company to physically locate most phones, not only during a 911 call, but any time the phone is on. This information is usually logged, and is usually available to government agencies upon request, often without a warrent.

Risks:
1. Logging of your position at all times.

Alternatives:
1. Tablets without cellphone chips do not have 911 support, so won't have these
   flaws.
1. Remove the battery from your phone, leave it at home, or use a burner phone so you're hard to target.


### Cellphones, other security flaws

Through a host of security flaws intelligence agencies such as the NSA have the ability to remotely modify the software of most cellphones on the market. It's complex, and also largely unknown *which* models require which types of access, but it should be assumed they can do this fairly easilly to any model phone. This tech seems to be getting deployed at protests (often via cell-site simulators) as well as being used in more clandestine operations. Once modified the agency [gains remote access to all features of the phone](http://money.cnn.com/2014/06/06/technology/security/nsa-turn-on-phone/index.html)

Risks: 
 1. The phone can "pretend" to turn off (unless you remove your  battery). Thus continuing to track movements via 911 support or whatever else.
 1. The agency can listen to the microphone or take pictures with the camera.
 1. The agency can "keylog" meaning intercept your messages as you type them, thus defeating encryption technologies such as Signal.

Alternatives (same):
1. Tablets without cellphone chips do not have this category of flaw.
1. Remove the battery from your phone, leave it at home, or use a burner phone so you're hard to target.

### Cellphones and GPS technologies
Traditional GPS technologies are one-directional (GPS, and Galileo from the U.S. and GlONASS from Russia). The reciever (e.g. your phone) is passive and never sends a signal back to the satteliate. Thus, you can use GPS without giving up your position. This is not true of the latest GPS system out of the Chinese corporation Baidou. This system is bi-directional, and can be used by the Chinese government track your position.

It is believed that Baidou enabled GPS chips add a security flaw similar to U.S. 911 support, the extent is unknown, but that they return the users position to the sattelite is highly probable.

Many new phone GPS chips have the new Baidou GPS feature.

Risks:
  1. The Chinese government can find out where you are.
  1. The Chinese government may be able to access other features of your device, including data, etc. (this is still unknown)

Alternatives:
  1. Find a phone that lists the GPS technologies it supports, and ensure it only includes GLONASS (Russia's system) , or U.S. GPS sattelite systems.

### CellPhone USB Charger Rooting Issues

Remember when we mentioned all devices are vulnerable to physical access? With cellphones, plugging the USB cable in to an unknown device may count as physical access. 

Risks: 
1. Some older phones have no protection, and anything plugged in to the USB port has full access to the device. Even newer phones are likely to have security flaws in this component. If that thing you plug in (such as a USB charger) has been modified by an attacker, they may be able to violate your device's security. Here's an [example](http://www.extremetech.com/extreme/157207-black-hat-hackers-break-into-any-iphone-in-under-a-minute-using-a-malicious-charger) 

Alternatives:
1. You could simply only charge your phone using your own adapters, computers, etc.
1. Depending on lifestyle this might not be an option though. So, alternatively, you can either [purchase](https://www.amazon.com/s/field-keywords=usb+data+block&tag=electronicfro-20) or [cut up an existing wire to make](http://www.instructables.com/id/How-to-make-a-USB-no-data-charger-cable/) a data block USB cable. They are casually known as USB condoms. This is a USB charger where the power lines connect to the device, but the data transmission lines are set up to not connect. If you want to transfer information from your computer to your phone, you will need another cable with the data lines intact.

# Communication Security 
## Email

## Realtime Chat
### Signal / Securing your SMS
Open source, peer-reviewed, and [endorsed by Edward Snowden](https://www.youtube.com/watch?v=j_kieJ-Ng2Q), [Signal](https://whispersystems.org/) is an easy first step for anybody interested in basic security. It has been on both the Android and iOS app stores for many years, and works with most phone OS versions.

Remember that until you have also authenticated your contacts using "verify safety numbers" (in the conversation settings on the android version) you can be sure whoever is getting your information gets it securely, but you will not have a guarantee that the person who is getting it is the person you want to get it.

Outside actors will be able to determine who you communicated with and when, but not what you said.

If your phone is hacked by something else (like maybe you downloading shady apps) your texts will still be readable by whoever has hacked your phone. That person could also gain access to your private keys.

If you get a new phone, you will currently have to re-do key exchanges. This is an issue with Signal, not with the underlying technology.

You can download signal on the app store or [through their website](https://whispersystems.org/).

### Threema (iOS, Android, Windows Phone)

Threema is a secured messaging system which focuses on also granting anonyminity and runs a full stack in-house in Switzerland, a very free country by internet standards. You don't sign up with any personal information, and you can only add people by learning their IDs. You can download their app from the app store or [their website](https://threema.ch/en).

### Wickr (iOS, Android, Windows/OSX/Linux Desktop)

Wickr is a secured messaging protocol where messages disappear after a period, like Snapchat except with privacy. Also like Snapchat, it can occassionally be a little fussy until you get use to it. You can download it in the app stores or [on their website.](https://www.wickr.com/personal)


### OTR (off the record)
[Pidgin (Windows and Linux)](https://www.pidgin.im/) and [Adium (OSX)](https://adium.im/) are pieces of software used to connect to many kinds of messaging accounts at once. This means you can be active on more than one Google Talk / Hangouts account at once. Facebook messenger can also be routed through it. Time travelers will be happy to know you can also have this interface handle AIM, MSN, ICQ and a lot more. Adium and Pidgin happen to be the same system reskinned for different operating systems, but this is a common piece of software, and you can find lots of other pieces that do the same thing.

The Pidgin/Adium system has a great plugin called OTR, which is written by the group [Cypherpunks](https://otr.cypherpunks.ca/). OTR means Off The Record, and turns on encryption end-to-end with anybody else who has installed the plugin. Remember that authentication is a differnet problem than security, and that you should make sure any new keys actually belong to your friends before discussing anything really important.

When your messages are encrypted, if you have them synched to your phone or other non-encrypted views, they will look like gibberish on your phone because your phone will only see the encrypted version.

Here is [how you set up OTR on Adium](https://adium.im/help/pgs/AdvancedFeatures-OTREncryption.html). The Pidgin setup is a little bit more involved. [Windows has its own installer](https://otr.cypherpunks.ca/index.php#downloads) which you run separately. [Linux instructions](https://ssd.eff.org/en/module/how-use-otr-linux) vary by distribution, but generally there is a separate package for pidgin with OTR already installed that is handled by your package manager. 

Pidgin is not as reliable as it could be for video chat, mostly because certain platforms don't properly support video chat in their APIs. If you want to have a video chat, you may want to sign onto the client through the old way, and run the chat from there. It will not be encrypted. 

### XMPP apps

XMPP is am open-source messaging archiecture designed to be secure. Both Google Talk and WhatsApp started as forks of this platform, and to this day you can connect to talk with XMPP users through a Google Talk account. 

To run XMPP, you will need a client (Pidgin and Adium will work). You will also need your own server, or somebody else's server to connect to. Remember that if you don't trust whoever is running your server, you aren't that far ahead of using one of the existing corporate services.

### Voice Chat

### Video Chat

## Web Browsing
Governments such as China outright block many websites outside their country. Governments like Pakistan are intercepting all outbound traffic before it leaves the country so they can watch it.

These measures are meant to help you keep access to content which a dictatorship does not want you to see.

### 3.1: DNS privacy leak
Domain name service.

The internet works based in IP addresses. When you visite a website like "www.google.com", your computer has to look up what IP to send traffic to to reach "www.google.com". To do this it uses DNS. Usually your machine asks the nearest router the question, if it doesn't know it passes the question on up the hierarchy, and eventually when someone has the answer they respond, that DNS server responds in kind, etc. until the nearest router tells your machine the answer.

This is important because DNS is not encrypted or authenticated. This means every DNS server on that chain
 1. Could lie to your computer and send it somewhere else
 1. Knows that you wanted to visit "www.google.com"

Note that even if you use HTTPS (discussed below) DNS is still leaking *what* website you are visiting. Same is true if you are using a VPN or TOR, as by default DNS will still flow directly out your computer, instead of over the encrypted link.

Solutions: If you are using a VPN, or TOR and do not want your traffic being seen on your local network or ISP (or the government agency monitoring your ISP), you'll need take extra steps.

// TODO: Add DNS proxy information here

### 3.2: HTTPS

HTTPS is encryption and authentication of traffic between your machine and a website. HTTPS is the reason that it's reasonable to use your bank's website, and expect that your internet provider (or local coffee shop) can't see your password

### HTTPS Everywhere (Firefox, Chrome, Android, Opera)

The EFF has created [a plugin](https://www.eff.org/https-everywhere) which always forces you to use the more secure version of a website when available. This means that people in the middle will be able to infer the domain name you are looking at (like www.example.com) but your behavior inside the website will be hidden. 

### Known security flaws
HTTPS authentication comes with some caveats. 

The basis for HTTPs authentication is trusting a few hundred corporations around the world. Authentication information for these companies is built in to your browser.

Each of these companies holds a "root" cert, which can sign other certs. By signing a websites http cert the root authority is saying "I say this company is who they say they are". A lot of these companies are not actually trustworthy, and many of these companies are closely tied to governments.

If an attacker redirected all traffic everywhere, they'd likely get caught, so these attacks are usually local... such as via [hotel wifi](http://www.zdnet.com/article/hackers-are-using-hotel-wi-fi-to-spy-on-guests-steal-data/). Thus, VPN will often work around it.z

### VPNs 

A VPN, or Virtual Private Network, is essentially a computer based somewhere else and a secure tube to it. All communications from your computer flow over this tube, and out the other computer, as if your computer were where the VPN computer is. You can use this remote computer's view to see whatever the internet looks like from the perspective of that computer. This means that if a website is blocked in your country, you can use a VPN to "get to the internet" in another country, and then see the website.

They are commonly used now to get around traffic shaping measures by your ISP (Internet Service Provider: aka Comcast etc). ISPs illegally (under net neutrality) throttle services like Netflix all the time. If you're using a VPN though, the tube traffic is flowing over a secure tube first, to another computer. Since the tube is secure (encrypted), the ISP can't *tell* what type of traffic it is. So, opening a VPN to a colo means that they can't really traffic shape your internt traffic, they can only turn the speed up and down monolithically, impacting all traffic in the VPN. VPNs are also used to make working on unsecured coffee shop wifi reasonable, and can be used to sidestep snooping by non-government actors, such as your school or workplace.

With a VPN, outside actors will still be able to see that you are sending data out of the country if they are watching the VPN. They will be able to tell who you are unless you somehow make it incredibly difficult for them to tell what computer is connecting to the VPN. If the VPN is compromised, outside actors will be able to see what you look at, and possibly change what you are looking at.

This is why you want the other end of your VPN to come out in a place not controlled by whoever you are concerned is spying on you.

To set up a VPN, you will need to get an endpoint (normally a rented machine in a data center) and to configure your computer so all traffic goes through that endpoint. We are working to figure out easy ways to make this technology accessible to less technical people. We reccomend [OpenVPN](https://openvpn.net/index.php/open-source/documentation/howto.html#quick). Other options are explained in [the AnonOps #OpNewBlood VPN tutorial](https://newblood.anonops.com/vpn.html), which is the best nontechnical VPN overview we have found. You may want to consider doing your own homework on what VPN provider you ultimately choose, since that website is accurate but a bit shady.

Iceland has shown an interest in being a center for digital freedom. Further research on the best VPN endpoints is appreciated, but for now, Iceland is advised for your endpoint.

### 2.3: TOR

TOR stands for "The Onion Router". [TOR]( https://www.torproject.org/) is software and accompanying network used to help acheive anonymity on the internet, most often used for webbrowsing.

The Weakness of a VPN, as noted above, is that the VPN provider knows exactly who you are, and can look at your traffic. TOR attempts to fix this flaw.

Imagine you use one VPN. Then, set up a VPN to another machine, and another.  When your traffic leaves your machine it's wrapped in 3 layers of encryption.  The first machine strips away 1 layer, leaving 2 more. second VPN another layer, and the third VPN yet another finally sending your traffic out on to the open internet. This is essentially how TOR works.

The idea is that the VPN machine knows who you are, but can't see your traffic. The last can see your traffic, but only knows the machine it's talking to, not who you are.  

#### TOR browser
The easiest solution for using tor is probably to install the [TOR browser](https://www.torproject.org/projects/torbrowser.html.en).

#### Known security problems

Government agencies are able to track down TOR communications, and have staged several [major crackdowns on illegal activity using TOR](https://www.wired.com/2014/11/operation-onymous-dark-web-arrests/). It is widely believed that the U.S. NSA is running a large portion of the nodes. TOR depends on that first and last machine not colluding, if both are machines run by the same people you lose.


# 4: Information Distribution, Verification, and Storage

# 4.0: Distribution and Protection Needs

Government removal of information from the internet is becoming increasingly easy. The United States government already has the infrastructure and authority to [seize domain names](https://www.justice.gov/usao-sc/pr/federal-court-orders-seizure-67-website-domains-involved-smuggling-and-selling-misbranded), effectively removing sites from the interent. 

The normal solution to this is to use a decentralized information network. Bit Torrent is one of the protocols often used to do this. This solves the problem of any one central point of failure, but anybody can put a torrent up, so you don't know if it is trustworthy.

Unfortunately, knowing if you can trust a file you download is a problem we have everywhere on the internet. Malicious people can switch out files on your network. This is why we also have systems to verify that a file has not been tampered with in transit, and that it comes from where you think it comes from.

Once you have sensitive information, you need secure ways to store it.

#### Wifi routers

Wifi router software is usually written poorly and quickly by amateur programmers. Government agencies and other hackers alike are now targetting wifi routers as they are so easy.

Solutions: Higher quality routers are harder targets for hackers, such as Google's product. Unless you are technical enough to be fairly sure it may be a good idea to treat any router much like hotel wifi.

## 4.1: Torrenting

## 4.2: Signatures and Checksums

## 4.3: Full Disk Encryption

Full disk encryption is exactly what it sounds like. To boot the machine you type a password which is stored in memory, and used to decrypt the data as it's accessed. This is useful if your security concerns include direct physical access to your

Under Linux most major distros now have an option to enable this during install.

Note that full disk encryption can save a lot of concern if a machine is physically lost, or fails in a way that makes deleting the data on the harddrive difficult.

### Weaknesses
Note that, there are still ways for someone with access to your machine may be able to get your data.

 1. Bus mastered protocols (firewire): If your machine is left on (sleeping usually suffices), an attacker with physical access can plug a device in to a bus-mastered the port. Older USB specs are not sufficient. This attack has been demonstrated with firewire, and it is likely that USB-C and Thunderbolt have the same flaw (since they seem to support bus-mastering). Since the key is stored in memory they can access it directly, or ask the system to decrypt the data for them and stream it to the newly plugged in device... accessing your data despite the encryption.

 1. 2 physical accesses: An attacker can remove the storage device and edit the bootloader to record the key in plaintext on the boot partition next time you start your machine. They then put the device back in to your machine. Next time they get access to your machine the key is right there, and they can access everything.

## 4.4: Getting Rid of Data / Destroying a Hard Drive

This is probably not generally necessary, as you are unlikely to get federal agents interested enough in your computer to come put your hard drives back together, but the guide wouldn't really be complete without this.

### Data Erasure

Deleting files does not mean they are gone from your computer. It only means that you have told your computer they aren't there. Until another program overwrites the space with more data, anybody with the right tools can recover the information.

Even after you overwrite the data the first time, people with large amounts of resources can still recover data. A state police lab will easily have these resources. This is why there are programs on the internet which will write your drive to entirely zeros, or even random junk data to your drive over and over again for you. Running these over and over again will decrease the odds that data can be recovered, but will not guarantee it.

### Physical Destruction

Physically destroying the drives is a good option, and in most cases just smashing the part which store the data is enough. However, if you have [really attracted some attention to yourself](http://www.popularmechanics.com/technology/security/how-to/a8566/how-to-read-a-smashed-hard-drive-14877558/), you should know that the relevant pieces of data can be stored on extremely small pieces of the drive, so it can be difficult to make sure you have properly destroyed the drive. There are two kinds of hard drives, and each have different relevant parts to destroy.

Corporations with serious data security concerns go through a fairly specific process. Best practice today is:
 1. Have the drive encrypted in the first place, just in case it goes missing.
 1. "Degause" the drive. This means to run very strong magnets over it over and over, flipping the field back and forth. This is similar (but much faster) than writing lots of random data over it repeatedly.
 1. Powder the drive. Meaning to literally grind the drive in to dust.

#### HDD: Hybrid Hard Drive (Old Kind)

The data is kept on a circular object called a platter. If you open the case, it is the large circular thing. Remove it (you can smash it to make it easier to remove, but that won't do it on its own). Watch out for the magnets, which are strong enough to break fingers if they become dislodged and rush together with you in the middle. Make sure you leave nothing connected to the center, as your data takes up extremely small amounts of space.

#### SSD: Solid State Drive (New Kind. Sometimes in desktops, almost always in laptops)

When you access a solid state hard drive's board, you will see a bunch of black computer chips which are likely symetrically mounted. Your data is stored in those chips. You can pry the chips off the board with a flathead screwdriver. Idealy you then smash these chips as well.

//TODO picture of a SSD because this is confusing

#### Destruction

There are a variety of options out there, but you can always smash the storage portions stuff up until a paper shredder will finish your job for you. 

#### Disposal

The bigger trick is making the pieces hard to find. Your can always take a nice drive down the freeway and pour the little remaining fragments out a window.

# 5: Internet Anonymity

## 5.0: Need

## 5.1: Remailers

## 5.2: Your IP Address

## 5.3: What Is a Clean Computer?

## 5.4: Tails

Tails is [live CD/USB software](https://tails.boum.org/) which has a lot of preconfigured privacy and encryption software. This means you'll set up a drive, reboot your computer to use that disk as a hard drive, and when it turns back on, your computer will be secured by default. Then, when you turn your computer off again and remove the drive, you can turn it back on again and access your files on your hard drive as normal.

# 6: Anonyminity for in Person Work

## Facial Recognition Software

## IMSI Catchers

When your phone connects to a tower, the tower knows which phone it is. Police forces now have fake towers which will record all phones which connect to them. This can be used to de-anonymize protestors. 

The best defense (inconvenient as it is) is to have a cheap burner phone which you only use for political action. Android phones are available for ~$60 now.

## Filming Police Conduct

While a few areas have made this legally difficult (and you should check) the [ACLU has provided software which will automatically upload any video you take and send it to your local ACLU chapter.](https://www.aclu.org/feature/aclu-apps-record-police-conduct)

It is advised that you use an auto-uploading app of some type, as police often confiscate phones with incriminating evidence on them.

## Cellphones
Can give up your position, as well as record other information about you, even while appearing to be turned off.

See cellphone sections under "Known Compromised Systems"

# 7: Legal

## 7.0 Description
The primary author is not a lawyer, and none of the colaborators are known to be one either. This document is not legal advice. 

## 7.1 No Fingerprint Readers to Unlock Things

## 7.2 U.S. Customs and border patrol
When passing through U.S. customs it's probably smart to assume all your devices may be siezed and searched.

Customs claims that since they can search your luggage, they can also search your devices. They extend this to include data stored in the cloud which your device has access to. 

Though it's not commonly done, they can and do take devices and image them, or they can hold you indefinitely until you agree to unlock a device so they can access the data.

For this reason burner phones and the like may be your best bet when crossing the U.S. border.

## 7.3 Passwords not necessarilly protected by U.S. 5'th ammendment
It's currently unclear whether giving up a password is protected by 5'th ammendment rights. There is at least one case where someone has been put in jail for over 2 years (as of now) for not giving up a password to data encrypted on his computer's harddrive (believed to be child pornography in this case).

# 8: Contributing to Internet Freedom (Mostly Nontechnical)

## 8.0: Explanation

Since many of these services are decentralized or crowdsourced, you can contribute by running a piece of the network.

## 8.1: Running a Tor Exit Node

This is a huge service to the public, but **does sometimes expose you to harassment from the US federal government.** One of the greatest concerns about the security of Tor comes from the number of exit nodes which are controlled by the US government, so helping run more non-government nodes is a very big deal. Here is [Noisebridge's guide on responding to federal inqueries about their tor exit node](https://www.noisebridge.net/wiki/Noisebridge_Tor/FBI). 

Please seriously consider [running a Tor exit node](https://blog.torproject.org/blog/tips-running-exit-node), particularly if you live in a country with stronger civil liberties. 

## 8.2: Downloading and Storing Activist Information for Offline Distribution

## 8.3: Running a Bittorrent Mirror for Activist Information

## 8.4: Configuring Your Phone to Detect IMSI Catchers
