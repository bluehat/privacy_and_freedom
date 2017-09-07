# A Citizen's Guide to Digital Freedoms

# Background

## What and Why
The goal of this guide is to help technical and non-technical people alike, particularly political and social activists, keep their information and communications confidential.

## Help Needed

 1. Technical people: We welcome contributions, additions and corrections.
 1. Non-technical people: Information about what areas are unclear or in need of improvement is hugely valuable.

Non-technical people: To contribute you can simply comment on github.

Technical people: First "clone" the repository on github, modify it as desired and then comment with a "pull" request. Sadly, gist lacks an explicit "pull request" feature, this is the closest we can get.

## Ownership and Distribution

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), though we'd prefer that you just submit patches to [this gist](https://gist.github.com/bluehat/76a07a5d25f038a89f3b99c54a9a94a9). If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate). All Amazon links include the EFF referral tag, so they get money.

This information is kept in git format because it is easy to transmit git repos peer-to-peer. You are encouraged to download a copy. Suggestions on how to keep the guide trustworthy and from having merge issues in a peer-to-peer environment are appreciated. 

# Terminology
## Security
Security is a very nebulous term, including concepts like financial security, so for our purposes we're going to stick to 2 particular types of security.

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

Here's some you probably know about;

 1. The location of all cell phones in the U.S.
 1. [The calling and called phone numbers of every phone call made in the U.S.](https://www.theguardian.com/business/2016/oct/25/att-secretly-sells-customer-data-law-enforcement-hemisphere).
 1. Most websites log the "internet address" of every machine that accesses them. They also usually log all major or interesting operations.

Here's some you probably don't:

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
 1. Install only a minimum of software you need, and get it from reputable places if you can. Any software you install could be malware. Software from an app-store is less likely to be a problem, as the corporation running the store is looking for them, but sometimes some slip by. Software you get from an email, or from a website an email pointed you to is very likely to be malware, even if it *looks* like a friend sent the email. We'll talk about email later on.
 1. Don't give your attacker physical access. All devices can be compromised given physical access, without exception, and usually in a way that would be nearly impossible to detect. Examples include keyloggers under the keyboard of a laptop, or in a replacement cellphone screen; firmware modifications to various hardware; Modifications of operating systems or applications; and the list goes on. Some modifications are not even removed to re-installing your O.S.

Some systems are known to have extant exploits, or even be "pre" crompromized from the factory, and aren't getting fixed for one reason or another. Here's a partial list of certain products and their associated risks as well possible alternatives.

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
### Normal Text Messaging
Cellphone type text messaging has a number of security flaws inherent in it's
design.

Risks:

 1. Cellphone companies can trivially log SMS, and probably do.
 1. Cellphone systems use extremely weak encryption (analogous to the rot13 example earlier), with no authentication. It's simple and cheap for an attacker on the same cell-tower to decrapt and listen using off-the-shelf hardware.
 1. The FBI or police are likely logging the messages *directly*. The FBI and police departments routinely use cell-site-simulators at rallies and protests now. These devices pretend to be the cell-phone-tower your cellphone would normally talk to. Your cellphone happily connects to this simulator, and the simulator thus gets your traffic, records it, and then forwards the traffic on to the normal phone network.

Result: Functionally you get none of Authentication, encryption, or anonymity.

### Signal (cellphones)
Signal is a cellphone app designed to replace normal texting, but adding in strong encryption and authorization. So when you send a message you know it's going to the person you send it to, and only them. Playing a little buzzword bingo, it's open source, peer-reviewed, and [endorsed by Edward Snowden](https://www.youtube.com/watch?v=j_kieJ-Ng2Q). [Signal](https://whispersystems.org/) is an easy first step for anybody interested in basic security. You can install it directly from the app-store on virtually any phone.  You can als download signal through the designer website [here](https://whispersystems.org/).

Earlier I said it's authenticated, but there's a catch. Before you get a strong authentication guarantee you have to meet with the person you want to communicate with and use the "verify safety numbers" (in the conversation settings on the android version) feature. Basically this step ensures that the Signal knows that it's authenticating everything to the right person.

If you get a new phone, you will currently have to re-do key exchanges. This is an issue with Signal, not with the underlying technology.

Risks:

 1. You're still on a cellphone, so keep in mind device security.
 1. Signal, the cellphone company, and the police running their cell-site-simulator can still see you are talking to your friend, just not what you are saying.

Result: Authentication, Encryption, but no anonymity.

### Threema (cellphones)

Threema is a secured messaging system which focuses on also granting anonyminity and runs a full stack in-house in Switzerland, a very free country by internet standards. You don't sign up with any personal information, and you can only add people by learning their IDs. You can download their app from the app store or [their website](https://threema.ch/en).

We haven't researched this app in detail yet, so more details are needed

Risks:

 1. Note that it's actually "pseudonomous" not anonymous. The IDs are persistant, and thus someone can see that ID1 is talking to ID2, and ID1 talked to ID3 yesterday... they just know who ID1 is.

Result: Unknown authentication, unknown encryption, partial anonymity.

### Wickr (cellphones, computers)

Wickr is a secured messaging protocol where messages disappear after a period, like Snapchat except with privacy. Also like Snapchat, it can occassionally be a little fussy until you get use to it. You can download it in the app stores or [on their website.](https://www.wickr.com/personal)

We haven't researched this app in detail yet, so more details are needed

### Google/Facebook web-based chat
What about just using the web interface to Google "hangouts", or Facebook chat?

Risks:

 1. See browsing security. HTTPS isn't all it's cracked up to be (poor
   authentication)
 1. Your text is encrypted only to their server, then decrypted. It's
   re-encrypted to send to the person you are chatting with. So, your
   conversation can be seen by the corporation.
 1. Note that by default your conversation is also logged by google, but you can
   turn this off by turning on "OTR"... Note that this OTR has nothing to do
   with the algorithm discussed earlier and just disables logging.
 1. A third part can see that you are talking, only google can see who you are
   talking to.

Results: Weak authentication, weak encryption, poor anonymity

### Facebook Messaging Phone app
Surprisingly, Facebook has added proper end-to-end encryption. This allows you
to encrypt your messages such that facebook can read them. To use this though,
you have to enable it every time you chat. 

Risks:

 1. Encryption is believed to be pretty solid
 1. Authentication is based on facebook ID, so as long as you make sure that
   facebook friend of yours is actually your friend, you should be good.
 1. It gives no anonymity guarantees
 1. It's on the phone, so watch that device security

Results: okay authentication, goood encryption, no anonymity

### Pidgin/Adium + OTR (computers)
OTR (Off The Record) isn't actually a chat system, instead it's an algorithm that can be used on top of most extant chat systems.  OTR is one of the very few examples of a communication system that supplies all
of encryption, authentication, and anonymity. Rather than being designed as a tool of corporate greed, it was designed as a research product, and subsequently peer reviewed... so it's about as solid of a system as you'll find. Details here: [Cypherpunks](https://otr.cypherpunks.ca/). It's been reviewed by numerous security professionals and non-professionals alike, including a group of CMU undergrads who got curious one evening ;-) .

Okay, it's not a chat system, so how do you use it? The answer is:

 1. Install [Pidgin if you're using Windows or Linux](https://www.pidgin.im/) and [Adium if you have an apple machine](https://adium.im/). These are actually the same codebase, just named differently.
 1. Install The OTR plugin for that piece of software.  Here is [how you set up OTR on Adium](https://adium.im/help/pgs/AdvancedFeatures-OTREncryption.html). The Pidgin setup is a little bit more involved. [Windows has its own installer](https://otr.cypherpunks.ca/index.php#downloads) which you run separately. [Linux instructions](https://ssd.eff.org/en/module/how-use-otr-linux) vary by the version of Linux, but generally there is a separate package for pidgin with OTR already installed that is handled by your package manager (if you run Linux, you probably know what that means). 
 1. To get solid authentication, you have to verify that the key you get is actually associated with your friend. 
 1. Chat with them using whatever chat system you like: AIM, MSN, ICQ, etc. 

This solution worked a lot better back when Facebook and Google used standard
chat protocols (namely XMPP)... basically, when they played nice. Unfortunately
they don't play nice anymore, so making this solution work with Facebook or
Google chat can be problematic. Also, note that there is no cellphone solution
listed, though you may be able to hunt one down, none are known at the time of
this writing.

Risks:

 1. Honestly, this is as good as security gets. Open source, peer reviewed software with no corporation in the middle. It uses the best anonymity, authentication, and encrytion algorithms available. We're down to device security.

Results: Everything you want security-wise

## Voice Chat
Many of the text chat systems support voice as well, and security is usually about
the same.

Cellphones, Facebook/google web interfaces all follow the same patterns. Pidgin/Adium don't do this very well.

## Video Chat


## Web Browsing
Lets talk about our three properties in the context of webbrowsing. When browsing:

 1. Authorization means viewing the website you were trying to view, rather than
   some other website.
 1. Encryption means no-one but you and the website knowing what you do on the
   website
 1. Anonymity means that no-one but you and the website know you even *visited*
   the website.

In webbrowsing there is a fourth property we want to talk about, and that is "Availability". Governments such as China outright block many websites outside their country. Governments like Pakistan, India, etc. are intercepting all outbound traffic before it leaves the country so they can watch it. So, while a website may be available to someone in the U.S. it may not be available to someone in China. 

#### HTTPS
HTTPs is the primary tool intended to supply authorization and encryption. HTTPs is often referred to as the "green lock" that most browsers show when you visit a website with this feature. This "green lock" means that your link is using HTTPs and thus theoretically ought to have both authorization and encryption. Unfortunately, HTTPs doesn't do it's job very well. It turns out that it's quite easy for governments, as well as a few special corporations, to flat out bypass the authorization IF they can manage to intercept your traffic. As bad as HTTPs is though for authorization, it's basically the only authorization tool we have at our disposal for most webbrowsing... so, we'll talk about how to improve these properties despite HTTPs' poor design. So, if you have a "green lock" you have encryption, but not authorization or anonymity, and depending where you are you may also lack availability of some sites.

#### DNS
When you visite a website like "www.google.com", your computer has to look up where on the internet that website is. To do this it uses DNS (Domain Name Service). Usually your machine asks the nearest router the question (like the wifi access point you have at home). If that device doesn't know it passes the question on up the hierarchy, and eventually when someone has the answer they respond, that DNS server responds in kind, etc. until the nearest router tells your machine the answer. This is important because DNS has no authorization, security, encryption, or anonymity... at all. Amazingly, despite a few very week/failed attempts to fix this, there are absolutely no provisions to make this process secure.

Note that each of the technologies listed may have other security gains. Here, to aid understanding, I'm listing them for their *primary* use.

### Improving Encryption
#### HTTPS Everywhere (Firefox, Chrome, Android, Opera)

HTTPS Everywhere is an add-on for your browser which makes sure your browser uses HTTPS whenever it can. Read more about it [here](https://www.eff.org/https-everywhere).

### Improving Authorization and Availability
Remember that I said that governments and some corporations can violate the authorization of HTTPS if they can intercept your traffic? That's an important if. There are methods to make that interception more difficult.

#### VPNs 
A VPN, or "Virtual Private Network", is essentially a computer based somewhere else and a secure tube to it. Most communications from your computer flow over this tube and out the other computer, as if your computer were where the VPN computer is.

There are several reasons to use a VPN:

 1. To route around censorship or spying: If the internet is censored or monitored in your country (e.g. China for censorship, U.S. for spying), but not in some other country, you can get a VPN in the other country. Then you can use this remote computer's view to see whatever the internet looks like from the perspective of that computer. This will allow you to access sites not available in your country. 
 1. To secure your link to the internet: When on public wifi (like a hotel or coffee shop), or other suspect wireless (See router information). You can use a VPN to make sure all traffic, over that part of the network at least, is encrypted and authenticated. Another example of this sort of use is if your internet provider is not trustworthy and is modifying traffic... such as making your online videos slow (netflix/youtube). 

For tech nerds: while you can rent a machine or VPS and set up your own VPN from scratch, it's an investment and it actually loses some anonymity gains a VPN might offer. If your goal is just to talk securely with your own server with strong encryption and authorization, this is a great option though. It does mean you can trust the provider though, assuming you trust your hosting provider.

For most people a better option is to rent a VPN. One apparently trustworthy and cheap option is [Private Internet Access](https://www.privateinternetaccess.com/). One advantage of using them is they have sites all over the world. You can just have it route traffic wherever it likes if your goal is #2 on my list above, but if it's #1 you can explicitly select a location. A good location to avoid spying and censorship is Iceland, as they have shown an interest in being a center for digital freedom. Note that PIA has simple setup directions for computers and phones of almost all types.

Risks:

 1. Internet providers, government agencies, etc. will still be able to see that you are sending data out of the country (if your VPN is out of country).
 1. If you use your own VPN they will be able to see who you are, if you use a heavilly traffic public VPN you make tracking down who you are that much harder (since your traffic is mixed with everyon else's), but not impossible.
 1. DNS doesn't flow over the VPN without a lot of extra work. DNS has no authorization, and violating DNS authorization is a useful step in violating HTTPS authorization.
 1. The usual Browsing leaks are still an issue 

Results: Might help with anonymity. It makes redirecting your traffic a little harder, so it's a small help to authorization. Can be used to route outside your country, so helps availability.

### Improving Anonymity
This is the hardest proerty to to get while webbrowsing.

There are a lot of things against you. What you do on wifi is visible to everyone using that wifi. Additionally it's visible to the Internet provider (the company you pay for "internet", like comcast or AT&T), and to lots of other corporations and government entities on it's way to the website.

Here are the major leaks to think about:

 1. DNS leak: When you visite a website like "www.google.com", your computer has to look up where on the internet that website is. To do this it uses DNS (Domain Name Service). Usually your machine asks the nearest router the question (like the wifi access point you have at home). If that device doesn't know it passes the question on up the hierarchy, and eventually when someone has the answer they respond, that DNS server responds in kind, etc. until the nearest router tells your machine the answer. Everyone I spoke of above, can see this request and answer.
 1. Your "Internet Address": When you get information from a website, you send information to the website about how to send information back to your computer... like a return address. Everyone I just spoke of can see this return address, even if you are using HTTPS.
 1. Logins: Now lets say you are using a website. Many websites require you to log in. This is a unique identifier that website can and will associate with everything you do on their website as they log it. As mentioned earlier, logs are often handed over to government agencies.
 1. Cookies: Many websites drop a "cookie" on your machine when you visit the website. This way if you visit it again they can tell it's the same person. Functionally this is just like a login for them, except you don't have to log in. 
 1. Advertising: Advertising often has trick code in it involving cookies or more subtle things to help uniquely identify you. These are particularly problematic as the same advertising company advertises all over the web, so the identifiers the assign to you aren't just for one website, but for sites all over the web.
 1. Browser identification: To help decide what information to show you, your machine tells websites a lot of information about your machine. What type of machine its, what type of browser it is, all the plugins you have installed, the dimensions of your browser window, etc. For those who think they know how to work around this, a lot of information is leaked via javascript rather than user-agent information
 1. Browser Leaks: One website you have loaded can tell what *other* websites you have open in the same browser.

Looking at that list, it becomes clear we have our work cut out for us. It's also pretty obvious that doing a perfect job is nearly impossible, so it's a matter of trying to do the best we can.

#### Don't log in to things
If you are trying to be anonymous... don't log in to things unless you have to.

Whatever you do do NOT log in to facebook, and then browse something you want to be anonymous. Before doing something anonymous, wipe all your browser data (cookies, etc.), close your browser, and open it again. Even better, use a seperate browser (like tor browser) only for your anonymous work, and only log in to anything on it when you HAVE to as part of that semi-anonymous/pseudonomous work.

Configuring your browser to dump all this information every time you close it makes this process easier. Chrome seems to have removed this feature, but firefox still has it.

#### Disable Cookies
In your browser settings you can disable cookies from all hosts, or just remove hosts. Note that this will break some websites, so you may want to do this only in the browser you use for your anonymous/pseudonomous work.

#### Disable most CA-certs
For tech people only, This is pretty advanced, and is a pain to maintain, but if you really want to get paranoid this is a great idea. If you don't understand this, don't worry, just move on.

The weakness in HTTPS relates to the root certificates built in to the browser. Chances are you don't need them all, especially for your anonymous/pseudonomous work. So, you can disable them. One good method is to disable them ALL. Then when you visit a website you need and https fails to authenticate, look up the cert information for that site. Go in and find that root cert, and enable it again.

For each root-cert you enable, you are allowing the owner of that root-cert to middle-man your HTTPS sessions, but at least this lets you control who that is. You may want to look up various root certs and associated companies to see what government they are associated with, Verisign is the U.S. for example.

#### Use TOR
TOR stands for "The Onion Router". [TOR]( https://www.torproject.org/) is software and accompanying network used to help acheive anonymity on the internet, most often used for webbrowsing.

The Weakness of a VPN, as noted above, is that the VPN provider knows exactly who you are, and can look at your traffic. TOR attempts to fix this flaw. Imagine you use one VPN. Then, set up a VPN to another machine, and another.  When your traffic leaves your machine it's wrapped in 3 layers of encryption.  The first machine strips away 1 layer, leaving 2 more. second VPN another layer, and the third VPN yet another finally sending your traffic out on to the open internet. This is essentially how TOR works. The idea is that the VPN machine knows who you are, but can't see your traffic. The last can see your traffic, but only knows the machine it's talking to, not who you are.

Unsurprisingly, with your traffic bouncing all over the internet and getting encrypted and decrypted over and over again, you're browsing experience is going to feel slow compared to normal. For this reason, while you could use it all of the time to make the fact that you are using it less suspicious, it's usually used just when you are doing something where you need it.

To use TOR we recommend using TOR browser, as it just works. Getting clean switching to turn it on and off, dealing with DNS leaks, and dealing other privacy leaks can be difficult and takes a fair bit of time and technical knowledge and skill. Feel free to go it on your own, but be aware that it's easy to screw up and leak something. If what you are doing matters, you'll want to spend some time being sure you got it right.

Risks:

 1. Government agencies are able to track down TOR communications, and have staged several [major crackdowns on illegal activity using TOR](https://www.wired.com/2014/11/operation-onymous-dark-web-arrests/). It is widely believed that the U.S. NSA is running a large portion of the nodes. TOR depends on that first and last machine not colluding, if both are machines run by the same people you lose.
 1. You're still vulnerable to the usual DNS leaks, javascript browser identification techniques, cookies, etc. The devil's in the details... see TOR Browser below.

Results: Similar to a VPN. It helps a lot more with anonymity but is also a little more likely to make you a target.

##### TOR Browser
The Tor Browser is The easiest solution for using tor. Read more [here](https://www.torproject.org/projects/torbrowser.html.en).

TOR browser is like any other web browser. It's the bit of software you load to view the internet, filling the same role as Internet Explorer (default on windows), Firefox (default on linux), Chrome, etc. You're old browser will still be present. How to install it and run it depends on your system, see the website for details. In all cases though, to use TOR you'll want to run the TOR Browser, rather than whatever you usually use to browse the web. To browse the web normally when you aren't worried about anonymity and all that, you can still load up your normal default webbrowser.

Note that the TOR Browser solves the DNS request leak for you, and even helps a bit with browser identification. In short, if you don't know what you are doing it "just works". Install it, and is use it, preferrably without configuring ANYTHING. That's about the best anonymity you can get.

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
