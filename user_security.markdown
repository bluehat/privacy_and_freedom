# A User's Guide to Security and Privacy

---
# Background
---

## What and Why

The goal of this guide is to help technical and non-technical people alike keep their confidential information confidential in our modern electronic world.

 * The "Basics" section is intended for anyone who uses a computer. This is about keeping your information confidential from average hackers. 
 * The "Advanced Topics" section is intended for more interesting use-cases such as political and social activists, reporters, etc. This is about keeping your information confidential from more powerful state actors, particularly things like your idenity and location.

If your head is realing after reading over "Basics" and you're just an average joe/jill, go ahead and call it quits. That said, if you followed it all though, we encourage you to at least skim the Advanced Topics. There's some very surprising information there that is not widely known. At the very least you can have fun blowing your friend's minds at dinner parties.

## Help Needed

 * Technical people: We welcome contributions, additions and corrections.
 * Non-technical people: Information about what areas are unclear or in need of improvement is hugely valuable.

As a github document, feel free to comment, fork and ask me to pull, etc.

## Ownership and Distribution

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), Though we'd prefer that you just submit patches to [this git repo](https://github.com/bluehat/privacy_and_freedom). If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate). All Amazon links include the EFF referral tag, so they get money.

This information is kept in git format because it is easy to transmit git repos peer-to-peer. You are encouraged to download a copy. Suggestions on how to keep the guide trustworthy and from having merge issues in a peer-to-peer environment are appreciated. 

## Disclaimer
The primary author is not a lawyer, and none of the collaborators are known to be one either. This document is not legal advice. 

---
# Terminology
---

## Security
Security is a very nebulous term, including concepts like financial security, so for our purposes we're going to stick to 2 particular types of security.

 1. Device Security: The inability for anyone to use or modify the software on a device you own, without your authorization.
 1. Communication security: The security of your communications with another person, to clarify what that means we break that down further below.

It's tempting to call things "secure" or "insecure" and you hear these terms used all the time by media and even by techies. Don't listen to it. In reality security is *always* a gradient. Something with all the best technology done the best way anyone knows may have a tiny flaw that no-one noticed.

A burglar breaks in to a house via the easiest method. A lock on the window doesn't help if the door is literally left wide open. Alternatively, A solid steel door with a fancy lock doesn't help if it's next to a glass window trivially broken. Similarly we measure a technology's security by it's *weakest* point, not it's
strongest.

Continuing the analogy most burgles don't come with ladders. There may be a use in using a steel door, even if the upper story windows are unlocked. For this reason we can't just talk about security as a single slider. It depends on who you are trying to keep things secure *from*.

This is all important because it's tempting to say "Ugh, everything is insecure". While that's true in a sense, we still lock our doors even though a burglar could use a wrecking ball. Even when we're talking about governments, dramatic measures get expensive, and often give away information a government doesn't want people to know (like that they just smashed up your house).  

Unfortunately, all this means we can't just say "Do this, it's secure", "don't do this, it's not secure". We have to explain the trade-offs. So, while we try and keep the explanations as simple as possible, we try and do so without washing out these important details.

## Communication Security
Communication security is made up of 3 components.

 1. Encryption: The inability for someone besides the person you are communicating with who sees your communication to understand it.
 1. Authentication: The assurance that you are communicating with the person you think you are.
 1. Anonymity: The assurance that no-one can tell who you are, or who you are talking to.

It should be noted that the 3'rd bullet here, though highly desirable, is rarely achievable, so in regular conversation the combination of 1 and 2 are usually considered "sufficient". For this document we'll try and spell out exactly what we mean rather than just calling something "secure" overall.

## Encryption
Encryption is a process by which you encode data such that it can only be understood again if you know some very large (and thus hard to guess) number. This number "unlocks" the encryption and thus is known as a "key". You can think of this number as having a certain number of digits.

If a hacker wants to access encrypted information, they are trying to guess that key, that number. If they simply try every possible number with that many digits that technique is known as "brute force", and the process of doing it is called "brute forcing the key". Usually encryption is designed to use keys FAR too large even for a computer to simply try all of the possabilities within a person's lifetime or even millions of years.

But hackers do "crack" encryption keys sometimes... how?

 1. It's important keys are actually large. It's pretty easy to try all the keys if they are only 1 digit. This means just because something is "encrypted" it's not necessarilly good encryption.
 1. We said we're using large number of digits so not even a computer can try all of the numbers within a person's lifetime... but what if someone has 100,000 computers working on it, and what if they are 100 times faster than the computer we were thinking of? They can do try all the possabilities 10 million times faster than we expected. This means that often if someone cares *enough* about getting your data and has enough money (like China or the NSA), they may be able to get it. Computers also get faster over time, so encryption gets easier to crack overtime.
 1. Every so often a hacker figures out a trick that allows them to elminate a whole lot of keys as possabilities, significantly reducing the number they have to try before they find the right one. You can think of this as basically reducing the number of digits in the number they are guessing.

We'll try and address how *good* a technology's encryption is. We generally consider an encryption technology good if we expect that no-one will have enough computational power, or find enough computational tricks, to guess your key within your liftime. 

## Availability
Security is one issue, and an important one, but it's not quite all encompassing. It's easy to make something secure by locking it in a steel box and burying it where no-one can find it. Availability is the important balancing factor.

In the context of communication this is whether it's possible to get a message to the person you intend. We generally don't talk about systems that aren't at least *okay* at this, so it won't come up much there.

In the context of web-browsing though it's much more interesting. Websites can be out there, but you may not be able to get to them. Governments such as China outright block many websites outside their country. Governments like Pakistan, India, etc. are intercepting all outbound traffic before it leaves the country so they can watch it. So, while a website may be available to someone in the U.S. it may not be available to someone in China.

When you are browsing the web usually you are trying to find some information, it's not a particular website you want, it's a particular piece of information. For this reason there is a third context that's important. This is "Information Availability". This is particularly interesting in light of various forms of censorship.

## Logging
Logging is technical terminology for the simple act of storing information. Almost every system in the technical world is constantly logging. It's pretty obvious why you might care about logging if you are worried about confidential information and communications. So, here are a few things that are logged, for you to keep in mind: 

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
This is a flaw in a piece of software or hardware, combined with a way to "exploit" that flaw to violate the security of a system (whether a device or communication system).

## Zero Day Exploit
Often shortened to simply "Zero Day". This is an "exploit" a hacker has found, but is unknown to the designers or general security community because they haven't used it yet. 

## Patch 
A fix for an "exploit". To say that an exploit has been "patched" means that it's been fixed. When you download and install a patch, or an update containing a patch, you are applying the fix to your system.

This terminology seems esoteric, but patching is VERY important. 

If you use good software and hardware, it will usually be fixed pretty fast once the designers find out there's a flaw. Zero day exploits are worth a LOT of money, so neither hackers nor governments want to use them if they don't have to. Instead, they'll use already known exploits taking advantage of the fact that users often don't actually install the patches. 

As a result, most real world security breaches use exploits that have already been patched. Just keeping up with patches (system updates) will put you far ahead of the game. We'll talk about this more in "Device Security".

## Attacker
An attacker refers to a person trying to get your confidential information. That is, they are trying to violate the security of some system that has the information.

We're going to use this term a lot. In our analogy earlier, we noted that most burglars don't bring ladder. It's important to understand who wants your confidential data, so you can understand what tools they have at their disposal... do they have a ladder?

## State Actor or "APT"
This is a specific category of "attacker". Once you're listening for it you'll hear this term pop up in the media a lot. "APT" stands for "Advanced Persistent Threat" and is usually assumed to be synonymous with "a country" (though it's not actually). Thus the other term "State Actor". The critical factor that makes an attacker an APT is that they have a LOT of resources to throw at trying to get confidential information. For example, a country can subpoena corporations and make them hand over info, physically threaten people, pay millions for black market zero day exploits, build enormous multi-billion dollar computers just for cracking encryption, etc.

If you are a loud political dissident trying to keep the U.S. government from getting your confidential information, you're dealing with a state actor. As an example, lets say you're organizing a protest group. While they will likely happily ask the phone company for a log of your location, log all your cellphone calls, spend a couple of physical people to covertly follow you around and see who you talk to in person, etc. You may still not be worth burning a zero day exploit on, or several days of a billion dollar datacenter to crack even poor cryptography. In short... a state actor probably has the "ladder" to reach your second story window. Keeping them out is going to be a bit harder.

Just because they have a ladder or wrecking ball though, doesn't mean they're willing to use it. When your opponent is in to the APT category, while the attacker has many resources, they have other priorities to spend them on and use of those tools may cause political problems. Even covert use of a tool that could potentially be discovered is a political risk evrey time. Keep that burglar in mind, what's the easiest path to your confidential information? Don't forget about options like declaring you a terrorist and arresting you. If that's politically feasible, it may be the open door next to the carefully locked window of your technology.

For these reasons, even in the case of a state actor, there are likely to be limits to what they can or will do, and thus there's hope in making your data "secure enough".

## Malware/Spyware/Trojan
Malware is any software designed to violate the security of your device. Two
specific types are spyware and trojans.

 1. Spyware refers specifically to software designed to watch what you do, like watching what you type on your keyboard, and usually sending that information over the internet to an attacker.
 1. A Trojan is a piece of software designed to allow an attacker to control your device remotely.

---
# Basics
---

# Device Security
We've defined device security, lets talk about why we care. First if you care about data on that device it's pretty obvious why this matters. More subtly though, if the attacker has direct access to your device, communications using that device aren't going to be secure. All the encryption and authentication you could use aren't going to help if someone can literally see what you are typing in the first place.

So, how do you keep a device secure?

 1. The #1 thing you can do to keep your device secure is to keep the software up to date. Remember the section on patching? Do it.
 1. Install only a minimum of software you need, and get it from reputable places if you can. Any software you install could be malware. Software from an app-store is less likely to be a problem, as the corporation running the store usually scans apps for malware, but sometimes some slip by. Software you get from an email, or from a website an email pointed you to is very likely to be malware, even if it *looks* like a friend sent the email. We'll talk about email later on.
 1. Don't give your attacker physical access. All devices can be compromised given physical access, without exception, and usually in a way that would be nearly impossible to detect. Examples include keyloggers under the keyboard of a laptop, or in a replacement cellphone screen; firmware modifications to various hardware; Modifications of operating systems or applications; and the list goes on. Some modifications are not even removed to re-installing your O.S. Examples of giving physical access include loaning your machine to a friend, or having it repaired (particularly at a less reputable shop).

Actually keeping a device secure, with so many interested in getting in to your device is surprisingly difficult. As a result there's a lot more information under "Advanced topics", including a number of devices that are easily compromised or compromised from the factory. Some of the weaknesses are very surprising.

That said, doing what's here will protect you from your basic opportunistic hackers. In our analogy equivalent to locking the door of your house.

## Lock Screen Timeout

While it's possible to get in to your machine given physical access, many attackers will be turned off significantly by a metaphorical locked door.  Whether on your phone or computer, it's a good idea (especially if you are ever in public spaces) to have the screen "lock" after some timeout.

On most systems this can be found somewhere in the settings menu. It may be under "security", "screen saver", or "power". If you can ignore your device for an hour, and go back to using it without typing your password, you probably don't have this enabled. Additionally, make sure that you must type in your password  if you put your machine to "sleep" and wake it up again (most laptops do this when you close the lid, they aren't off, just idle). To test just put it to sleep, wake it up, and see what happens.

Ideally when you stop using your device you should manually lock it. And leaving devices unattended in public is not a good idea for reasons already mentioned.  Closing the lid on laptops will usually put it to sleep, and lock it as mentioned above. But, enabling a timeout will help when you absentmindedly go to the bathroom in a coffeeshop, leaving your laptop on the table, or if your phone falls out of your pocket.

Risks:
  1. No increased risk, the only downside is possible occasional mild annoyance.

Conclusion: Everyone should do this if their machine is ever in a public space. 

## Fingerprint readers and facial recognition (biometrics)
We do not recommend use of biometrics (fingerprints, facial scans, etc.) for security.

 1. Every time biometrics are used, the technology is bypassed trivially not long after. For example, many early fingerprint readers could be cracked using a gummy bear handled by you.
 1. You leave behind your biometrics everywhere you go. Pictures or even 3D scans of your face can be grabbed quite easily. Fingerprints can be taken off anything you've grabbed. Given the fact that #1 is inevitable (regardless of what a company's advertising says), this poses a serious problem.
 1. You cannot rotate biometrics. If you know them to be compromised, you cannot change them.
 1. It's not something you know, but something you are. If an opponent has *you* they don't need you to talk, they can simply press your finger on the pad. This likely bypasses the courts, and means 5'th amendment rights in the U.S. probably won't apply *at all* when *maybe* they would apply with a password.
 1. Lastly, do you REALLY want the end-game to be someone kidnapping you and chopping off your finger? Leaving that as the best option for someone trying to bypass your security might not be a great idea.

Currently this is most relevant for device unlock e.g. unlocking your phone. It's also most likely to come up for protesters or those crossing a border who are seen as suspicious. In these cases having your unlock be a nice long PIN will likely give you a chance to get a lawyer and assert your rights, before the police get access to everything (once again, we're not lawyers).

## Disable device features you aren't using
A simple step to significantly increase device security is to disable stuff you aren't using. Having Bluetooth on exposes you to a class of security vulnerabilities (one called BlueBorne is unpatched in Android as I write this). If you aren't using Bluetooth, turning it off makes it nearly unexploitable. Same is true for WiFi, near field communication, and most other protocols.

You don't have to hobble yourself. If you use Bluetooth or WiFi every day, it might not be worth it to you to disable it if your security needs are not extreme. But few users use ALL of these things regularly, thus turning off the ones you don't is low-cost for a nice security advantage.

## Full Disk Encryption
Full disk encryption is exactly what it sounds like. To boot a machine with full disk encryption you type a password. That password is stored in memory, and used to decrypt the data as it's accessed. This is useful if your security concerns include direct physical access to your computer. Full disk encryption can save a lot of concern if a machine is physically lost, or fails in a way that makes deleting the data on the hard drive difficult.

Due to the ease of use and the utility in cases of perfectly routine loss, theft, machine failure, or just giving your old computer to a friend, everyone using a system that supports it easily should probably use disk encryption.

On Apple computers you can simply enable this at any time and it will convert the whole drive to being encrypted. Under Linux most major distributions now have an option to enable this during install. Windows has several 3'rd party products available to do this as well, but it may be a bit more complex to set up.

Risks (This is a bit technical, don't worry if it doesn't make sense):
 1. Bus mastered protocols (FireWire): If your machine is left on (sleeping usually suffices), an attacker with physical access can plug a device in to a bus-mastered port. Older USB specs are not sufficient. This attack has been demonstrated with FireWire, and it is likely that USB-C and Thunderbolt have the same flaw (since they seem to support bus-mastering). Since the key is stored in memory they can access it directly, or ask the system to decrypt the data for them and stream it to the newly plugged in device... accessing your data despite the encryption.
 1. Two physical accesses: An attacker can remove the storage device and edit the bootloader to record the key in plain-text on the boot partition next time you start your machine. They then put the device back in to your machine. Next time they get access to your machine the key is right there, and they can access everything.

Conclusion: It's not magic, but it's hugely helpful in a myriad of circumstances. Use it if your system makes it easy (Apple and Linux machines at least).

## Phone Encryption

Most phones now have the option of encrypting the entire storage device. This is basically identical to "Full Disk Encryption" for computers.

As with computers, there are very few downsides to using this, and we recommend everyone enable it. 

 1. Google (android) phones: Go to Settings -> security -> Encrypt phone. and enable it
 1. Apple phones: You should already have a PIN set (lock screen section above). Once this is done, encryption should be on, but you may want to double-check.

## What Apps
We mentioned not to install software you don't need, lets go in to a little more detail about that.

Obviously we all install some things because "maybe I'll need to do that later". If you're installing basic tools on say... an ubuntu linux system, everything is coming from a signed app repository and is highly unlikely to be malware. It's still a good idea not to install things you don't use, since every extra piece of software may have it's own security flaw, but it's not that big a risk.

On phones however, there's a LOT of malware out there in app stores. It's not as bad, but much closer to just downloading apps you find on random websites. Apple and Google both work pretty hard to keep malware of their app-stores, but they don't always succeed. The less software you install, the less likely you are to trip over something that they missed. This doesn't mean you should keep your phone blank, but if you can just use a web-interface on your phone to do something and it works fine, or the app is merely cute and not actually useful, it might not be worth installing. Just stick with the stuff you use and need.

There is one other feature of phone apps to look out for, and that is advertising. Ad content is grabbed off the network on the fly, this means that each time you open the app your phone is reaching out to the world and trying to download an ad to show you. So, the app pulls down some content that probably hasn't been reviewed by a human. That content can be malicious. In theory this shouldn't be a problem, but in practice it's hard to figure out all of the different things the ad content might try to do... as a result we recommend against running apps that display ads.

# Communication Security 

## Web Browsing
Lets talk about our three properties in the context of web browsing. As mentioned under "Terminology", for web browsing we also add a 4'th property "Availability":

 1. Authorization means viewing the website you were trying to view, rather than
   some other website.
 1. Encryption means no-one but you and the website knowing what you do on the
   website
 1. Anonymity means that no-one but you and the website know you even *visited*
   the website.
 1. Availability means the ability to get to a website

In this section we'll talk about #1 and #2 as these are what most people are worried about... what is colloqually called getting "hacked". #3 and #4 we'll leave to "Advanced Topics".

First, lets talk about how things work at their base, and some of the problems that arise.

#### HTTPS

HTTPS is the primary tool intended to supply authorization and encryption. HTTPS is often referred to as the "green lock" that most browsers show when you visit a website with this feature. This "green lock" means that your link is using HTTPS and thus theoretically ought to have both authorization and encryption. Unfortunately, HTTPS doesn't do it's job very well. It turns out that it's quite easy for governments, as well as a few special corporations, to flat out bypass the authorization IF they can manage to intercept your traffic. As bad as HTTPS is though for authorization, it's basically the only authorization tool we have at our disposal for most web browsing... so, we'll talk about how to improve these properties despite HTTPS' poor design. So, if you have a "green lock" you have encryption, but only poor authorization and no anonymity, and depending where you are you may also lack availability of some sites.

#### DNS

When you visit a website like "www.google.com", your computer has to look up where on the internet that website is. To do this it uses DNS (Domain Name Service). Usually your machine asks the nearest router the question (like the WiFi access point you have at home). If that device doesn't know it passes the question on up the hierarchy, and eventually when someone has the answer they respond, that DNS server responds in kind, etc. until the nearest router tells your machine the answer. This is important because DNS has no authorization, security, encryption, or anonymity... at all. Amazingly, despite a few very weak/failed attempts to fix this, there are absolutely no provisions to make this process secure.

### WiFi access points

WiFi router software is usually written poorly and quickly by amateur programmers. Government agencies and other hackers alike are now targeting WiFi routers as they are so easy.

Because of this, someone may be watching everything you do online via that router. So, you may want to treat even your own home WiFi like you were in a hotel or coffee shop (see VPN and TOR).

### Improving Encryption
#### HTTPS Everywhere (Firefox, Chrome, Android, Opera)

HTTPS Everywhere is an add-on for your browser which makes sure your browser uses HTTPS whenever it can. Read more about it [here](https://www.eff.org/https-everywhere).

# Web Services
We talked about web-browsing security, but these days the internet allows for a lot more interesting services. A lot of people access email using websites, edit documents, store data, etc. These sorts of services present some additional challenges that it's worth stopping to talk about. As we mentioned earlier, virtually everything you do online is logged. This is particularly true for web services. 

Suffice to say that the U.S. government can get these logs, and the company not only won't, but *can't* tell you about it. If this sounds crazy here's the legal background (though again, we are not lawyers). In the U.S. under the 3'rd party doctrine at the time of this writing this doesn't even require a warrant, just a subpoena issued by a secret court, not subject to freedom of information requests. All that said, you may not be concerned about the U.S. government, but some other government. Alternatively you may just want to keep your data secure from hackers. Lastly, this does take effort, and the government can't (currently, as far as we know) make sweeping requests, they have to be targeting you.

Data you have stored in a web service (and associated logs), are most vulnerable to much simpler attacks. Thus, the basics of password security, though not perfect protection, do matter and are worth getting right.

## Passwords
Lets talk about the 2 most common ways that people's accounts get "hacked"...
that is, that a 3'rd party, without legal means of getting your data, gets it
anyway.

 1. Lets say you use the same username and password on mail.google.com, as well as crappy_website.com. crappy_website.com has crappy security, so hackers are able to steel the usernames and passwords of all of the users. They then try this on other sites, and soon have logged in to your mail.google.com account.
 1. Hackers trying to log in to your account start guessing passwords, using software that does this extremely fast. Now, this would still take FAR too long, but they can speed it up if they steel something called a "hash" file, which is how well designed systems store passwords. While Hackers start with English words, they also know all of the usual tricks you use. They'll substitute "0"s for "O"s and "1"s for "i"s. They'll also try phrases, or the first word of every letter from famous sayings or texts.

What this means is that it's crucial that you passwords are all different, and that they not use any trick that might make them possible to remember, because every trick you can think of the hackers already know about.  I'm going to say that again, because this is really important... If you can remember your password, IT IS NOT GOOD ENOUGH. Everything else you've heard as advice about picking passwords is wrong.  

What to do then? This sounds kind of hopeless, but we have an answer: Use a password database, sometimes called a password vault.

### Password database
A password database

 1. Stores all your user-name and password combinations along with the sites they
   match
 1. Allows you to generate long, truly random, passwords that are thus 
 1. Stores the data in a way that it's hard to crack in to even using the tricks
    mentioned above, and given physical access to the device you store it on.

Ideally your password database will also get backed up somehow, because losing
access to ALL your accounts would be bad!

We have a couple of specific recommendations

#### LastPass

This is the simplest, solution. It's free for use on your computer, but involves a small yearly subscription fee for using it on your phone. Everything is stored online, and automatically synced between devices. It also has nice browser plugins making using those passwords easy while you are actually browsing.

For most users this is a great solution, but if you've been reading carefully you should be shaking your head about now. We were just talking about the dangers of using web services, can't the government get all your passwords? Isn't it logged every time your device checks in with the service to see if there's more stuff to sync? Wouldn't someone watching be able to use that request to identify your computer and discover you?

LastPass does do things right, the passwords are all encrypted with master passwords, making them very hard to steel if someone gets in to their network. But, it's a web service, so those worries are not unwarranted. For this reason you may want to use LastPass

Risks:
  1. It's a web service, with all of the risks this comes with.
  1. All your passwords are in one place, so if someone DOES get in, you're in trouble

Conclusion: A good choice for most people. Very easy to use and set up, but with some risks related to using a web service

#### KeePass

KeePass is a slightly more complicated "do-it-yourself" solution, but in return it's completely free, and you get full control over exactly where things are stored, who has access, and how you synchronize between devices.

Again it works on virtually all computers and cellphones. Many implementations are open source, and the method for encrypting the database was designed by and has been reviewed by the best security experts. There are a couple of versions available for some systems. Here's our suggestions:

 - Linux: KeepassX
 - Apple Computer: KeePass2
 - Windows Computer: Keepass2
 - Apple phone: KeePass touch
 - Google (android) phone: KeePass2

The most secure option is to manually copy database files around from one device to another, but that's pretty onerous for most users. So, our recommendation is to store your database in Dropbox, as this is a reasonable balance. Depending on your security needs a different option may be better for you though.

Unfortunately, this process is NOT as easy as one might hope, so you may want a technical friend to help you out. Just don't let them pick or see any of your passwords!

We're going to go through setting this up on a laptop and a phone. We would point you to a "howto" but most of them put the keyfile in the wrong location. As an example:

 1. Install and set up Dropbox on your laptop
 1. Install the correct version of KeePass on your laptop
 1. Start up the KeePass software on your laptop
 1. Create a database with a password AND a "keyfile". Name the keyfile ending with ".key". When creating the database make sure it ends up in the synced Dropbox directory, when creating the keyfile make sure it does NOT end up there.
 1. Install the correct version of KeePass on your phone
 1. Get the "keyfile" on to the phone, but don't use Dropbox to do it. This is the hardest part, and unfortunately can be a major sticking point. Every combination of phone/laptop though is different. 
 1. Tell the phone version of KeePass to use Dropbox for the database, and point it at the keyfile

It's FAR easier to put the keyfile on Dropbox, but also FAR less secure (if you are going to do use this, LastPass may be a better option if you don't mind the money). A hacker who gets only the database, even a government entity, is highly unlikely to ever be able to see your passwords. But, if they HAVE the keyfile, they can use the methods explained under "Passwords" to crack in, and then they'll have ALL your passwords!

With this setup you'll be able to access all your passwords offline. If the Dropbox app isn't started when your laptop starts there will be no synchronization, so nothing to give you away. This gives you a fair amount of direct control. 

One last note: We *strongly* urge you not to "autogenerate" passwords for a month or so. It's fairly common for people to lock themselves out of their password databases when they are getting used to the idea. So, keep your passwords somewhere else as well, until you are comfortable with it. Then you can replace your passwords one-by-one with autogenerated passwords by going to each website and going through the "change your password" dialogs.

Risks:
  1. All your passwords are in one place, so if someone DOES get in, you're in trouble

Conclusion: A better choice IF you are willing to deal with the extra hassle of setup. It's a bit more secure, and gives very fine-grained control over ease-of-use vs. security trade-offs.

## Email
These days most people use Gmail or Yahoo mail. If you and your friend both use gmail your security is actually pretty good since it's staying inside Google's network. But, lets see where we might have a problem.

 1. Google has the data, if they get a government subpoeana they have to hand it over.
 1. Remember that you just used HTTPS as the only security between you and gmail. We talked about the security problems with HTTPS. There's lots of things we can do to try and make it better, but in the end it's pretty flawed.

If you send email to any OTHER system, the email is sent from one system to the other in plain-text over the open internet. In other words, the government can and will trivially intercept the message and see it, if they think it's interesting.

We'll talk about ways to improve email security in "Advanced Topics"

### Email Authentication
Email has no authentication built in. Nearly everything you see when you look at an email can be faked. This means that just because the "from" section has your friend's email, the email could actually be from an attacker. Never completely trust email. A common hacker technique is to send an email that looks like it's from some service you use, like facebook or your bank. The email often has a link that looks like it points to that website... but if you look really closely it's not *quite* right, like maybe it's facebook.foo.com instead of facebook. 

Because of this, good policy is not to click any such links unless you were expecting the email. For example, if you just signed up for the service and they said they would send an email to confirm your email address, go ahead and click the link, but if you signed up last week or year... don't.

If an email seems suspicious to you, particularly if it asks for info, or points to a website that asks for info, there's a good chance it's actually from a hacker. If it's from a friend you can always ask your friend via some other communication medium if they really did send that email, before clicking through a link. If it's from a company you can often visit their website directly (without using the link) and navigate to the right place from their front-page, thus protecting you from a "fake" webpage with a link that looks legitimate.


# Anonymity for in Person Work
This is about how technology, either what you are carrying yourself, or what others have, may be used against you, or to your advantage for normal in-person non-electronic type work. Largely this section is about realizing what is out there to be concerned about.

## Cellphones

If you own a cellphone (which you do), and care about anonymity, or the security of in person interactions, conversations, etc. please read the "Advanced Topics, Device Security" sections relating to cellphones. This is relevant even if you aren't using your device, and even if it appears to be turned off! You should think of a cellphone as a surveillence device (microphone/camera/etc.) belonging to government entitites, which may at any time be recording your actions including using microphone, camera, and tracking your location.

## Photos

Most cellphones and many tablets these days have a GPS built in (global positioning system). A GPS When you take a photo with your cellphone, it will usually "tag" the photo with your GPS coordinates, that is with your position in the world when you took that photo. This tag is not visible when you view the photo (so you can't visibly verify it's not there), it's just extra data that's stored with the photo. If you post that photo online, or give it to someone, it's easy to read those coordinates back out and find out where you were when you took that photo.

Your cellphone also usually adds another tag as well, stating the type of device that took the photo. Again, if you post the photo online or give it to a friend, it's easy to see what type of device took the photo. To illustrate why you might care, and how easy it is even for experts to miss this kind of detail, executives of major tech companies have repeatedly accidentally leaked new hardware the company was developing by posting photos taken with those devices.

Alternatives:
  1. The first feature can be disabled on most phones from within the phone app. Unless you use this feature, we recommend simply disabling it on your phone. That way you won't forget about this subtle information hidden in your photos sometime in the future. 
  1. The second feature usually can't be disabled. While it may leak some information about who you are, if you're using say... an iphone... lots of other people do to, so it's probably not that big of an issue. If you're really concerned converting to a different format will probably drop the tags.

## Facial Recognition Software

Facial recognition software has gotten good enough to easily identify your face in any pictures taken with you in them, even with only a portion of your face.

This means you can easily be outed by someone's well-intentioned post to social media, happening to pass by a security camera, a police car camera, a police body camera, etc. Depending on where you are located traffic cameras may or may not record all the time, and may or may not be reviewed by authorities.

## License plate recognition software

This is used at all border stops within the U.S. (you do not have to cross a border to cross a border patrol stop). It's also used on many bridges now for tolls. Additionally you'll often see cameras pointed at the highway as you cross state boundaries, and probably many other places. Consider the possibility of this being used anywhere facial recognition software might be used. Police body cams, car cams, security cameras, etc. 

## Filming Police Conduct

While a few areas have made this legally difficult (and you should check) the [ACLU has provided software which will automatically upload any video you take and send it to your local ACLU chapter.](https://www.aclu.org/feature/aclu-apps-record-police-conduct)

It is advised that you use an auto-uploading app of some type, as police often confiscate phones with incriminating evidence on them.

---
# Advanced Topics
---
# Device Security
As we mentioned earlier, some systems are known to have extant exploits, or even be "pre" compromised from the factory, and aren't getting fixed for one reason or another. Here's a partial list of certain products and their associated risks as well as possible alternatives.

You may notice a lot of cellphone issues are on this list. This is partly because of the nature of the U.S. FCC regulations and closed specs of cellphone chips... but it's also because everyone uses a cellphone these days, and so governments have a huge incentive to figure out how to get information from them. Figuring out how to exploit systems is expensive so it's far more useful to build exploits for commonly used systems. Less used systems are less targeted, because the work is the same for less gain.

## Tails
Trying to secure a device is difficult, even for highly technical people. If you just want to read a webpage anonymously, you might consider using Tails. To use tails you simply download it and put it on a CD or USB-key, reboot your machine and boot it (to bring up this option try hitting "f1" "f2" or "f12" during boot until one of them brings up a menu with the word "Boot" in it and "USB" as an option... select it). This has several advantages. Tails is set up specifically for this purpose, so it's all configured pretty ideally for you, no work necessary. Additionally, since you are only using the system for this type of thing, not installing software on it, there are fewer avenue's for hackers to drop malware on it.

You can download it [here](https://tails.boum.org/). Tails is basically already set up "right" to be about as secure as you can get. 

When you are done you can simply remove the CD or USB-key, reboot your computer, and you go back to your everyday life. 

Risks:
1. Tails isn't going to save you from a completely compromised device. It helps as noted above, but only so much.
1. Tails does nothing special to avoid correlating browsing information.

Conclusion: If this meets your needs, it's a fast work-around to a lot of complicated setup that's easy to get wrong, much like tor-browser (which we'll talk about later) but even more so. But, it's not magic so you still need to understand a few things.

## "Find my Iphone" and similar services

These services allow a corporation to tell you where your phone is if you lost it. Many of them will also allow the corporation to disable the phone. It's no surprise then that they can do these things when you *haven't* lost your phone as well. This means if a hacker can compromise that companies security (a common occurance), the hacker can do these things. And the government can lean on the company to do these things.

For these reasons we suggest disabling any such features on your phone. 

## Known Compromised Systems
### Windows 10
[Windows 10's EULA stipulates that everything you do on your computer will be logged by Microsoft, and that these logs will be available to the government.](http://www.newsweek.com/windows-10-recording-users-every-move-358952).

Windows is what most laptops you might purchase would come with, so this basically means nearly all factory laptops. Don't worry though, there's some reasonable work-arounds.

Risks:

 1. Everything you do may be logged, and that log may be subpoenaed (or just
   requested) by a government, or lost to a hacker who infiltrates Microsoft.

Alternatives:

 1. Apple computers are one option, though they are quite expensive, and you're still trusting just a single company. On the other hand, some company had to build the hardware, and you have to trust them anyway.
 1. Some laptops can be had with Linux pre-installed. These are usually more than their windows competitors, but may be cheaper than Apple machines. Linux is not made by a single company, and many experts read and modify it looking for security flaws. On the other hand, this does give government agencies an opportunity to add security flaws.
 1. Buy a normal laptop, and install Linux on it for free.

Obviously installing Linux is a bit of complex affair, and likely requires a technical person. That said, it's no harder to use once installed than Windows or OS-X, and most software you'd want to use on it is free... Having a friend help you out may be a good option.

### Lenovo Laptops with Windows

Lenovo laptops have a [history of manufacturer-bundled malware](http://www.theregister.co.uk/2015/08/12/lenovo_firmware_nasty/) which opens a security vulnerability on the system if the system boots Windows. The code is injected before Windows launches. It is considered a malware and it is baked into the physical boards they ship you. This practice has gone on for multiple years, and has caused some [US federal government branches to try to not use the systems anymore](http://www.wsj.com/articles/u-s-navy-looks-to-replace-ibm-servers-for-security-after-lenovo-purchase-1432047582). [Obama has required that several federal agencies get approval for any systems they purchase if the systems are made in China](http://www.reuters.com/article/us-usa-cybersecurity-espionage-idUSBRE92Q18O20130328), supposedly for this reason. 

Risks:

 1. The malware adds a major security flaw to what would otherwise be secure web browsing. This means an attacker may have easy access to modify what you see on the web, including what software you download... functionally compromising the entire device. 

Alternatives:

 1. Install Linux on a Lenovo laptop, or buy a machine made by any other company.

### Cellphones, U.S. 911 support

All cellphones sold in the U.S. are required by law to have 911 support. Ostensibly this is a suite of features allowing a caller to call 911 on any phone without unlocking the phone, having a cell plan, etc. and allows the 911 operator to locate the phone when such a call is made. Most phones sold outside the U.S. are still legal for sale here, and thus still include this feature.

The features that allows this though also allow the phone company to physically locate most phones, not only during a 911 call, but any time the phone is on. This information is usually logged, and is usually available to government agencies upon request, often without a warrant.

Risks:

 1. Logging of your position at all times.

Alternatives:

 1. Tablets without cellphone chips do not have 911 support, so won't have these flaws.
 1. Remove the battery from your phone (if you can), leave it at home, or use a burner phone (one you throw-away after use) so you're hard to target.


### Cellphones, other security flaws

Through a host of security flaws intelligence agencies such as the NSA have the ability to remotely modify the software of most cellphones on the market. It's complex, and also largely unknown *which* models require which types of access, but it should be assumed they can do this fairly easily to any model phone. This tech seems to be getting deployed at protests (often via cell-site simulators) as well as being used in more clandestine operations. Once modified the agency [gains remote access to all features of the phone](http://money.cnn.com/2014/06/06/technology/security/nsa-turn-on-phone/index.html)

Risks: 

 1. The phone can "pretend" to turn off (unless you remove your  battery). Thus continuing to track movements via 911 support or whatever else.
 1. The agency can listen to the microphone or take pictures with the camera.
 1. The agency can "key log" meaning intercept your messages as you type them, thus defeating encryption technologies such as Signal.

Alternatives (same):

 1. Tablets without cellphone chips do not have this category of flaw.
 1. Remove the battery from your phone, leave it at home, or use a burner phone so you're hard to target.

### Cellphones and GPS technologies
GPS stands for Global Positioning system. When you use your cellphone to get directions using an app like Google Maps, GPS is how your phone can tell where you are on that map. It usually gets the map itself from the cell network, which is why you need cellphone service, but it figures out where you are on that map using GPS. Traditional GPS technologies are one-directional (GPS, and Galileo from the U.S. and GLONASS from Russia). The receiver (e.g. your phone) is passive and never sends a signal back to the satellite. Thus, you can use GPS without giving up your position or any other information. Your phone is not "communicating" with the GPS satellites, it only recieves a signal, never sends. It's like listening to someone talk, but never talking yourself.  All this is to say that Traditional GPS technologies are completely safe. They have affectively perfect security and anonymity.

BUT... This is not true of the latest GPS system out of the Chinese corporation Baidou. This system is bi-directional, and can be used by the Chinese government track your position.  It is believed that Baidou enabled GPS chips add a security flaw similar to U.S. 911 support, the extent is unknown, but that they return the users position to the satellite is highly probable.

Many new phone GPS chips have the new Baidou GPS feature.

Risks:

 1. The Chinese government can find out where you are.
 1. The Chinese government may be able to access other features of your device, including data, etc. (this is still unknown)

Alternatives:
 1. Find a phone that lists the GPS technologies it supports, and ensure it only includes GLONASS, or U.S. GPS satellite systems.

### Cellphone USB Charger Rooting Issues

Remember when we mentioned all devices are vulnerable to physical access? With cellphones, plugging the USB cable in to an unknown device may count as physical access. 

Risks: 

 1. Some older phones have no protection, and anything plugged in to the USB port has full access to the device. Even newer phones are likely to have security flaws in this component. If that thing you plug in (such as a USB charger) has been modified by an attacker, they may be able to violate your device's security. Here's an [example](http://www.extremetech.com/extreme/157207-black-hat-hackers-break-into-any-iphone-in-under-a-minute-using-a-malicious-charger) 

Alternatives:

 1. You could simply only charge your phone using your own adapters, computers, etc.
 1. Depending on lifestyle this might not be an option though. So, alternatively, you can either [purchase](https://www.amazon.com/s/field-keywords=usb+data+block&tag=electronicfro-20) or [cut up an existing wire to make](http://www.instructables.com/id/How-to-make-a-USB-no-data-charger-cable/) a data block USB cable. They are casually known as USB condoms. This is a USB charger where the power lines connect to the device, but the data transmission lines are set up to not connect. If you want to transfer information from your computer to your phone, you will need another cable with the data lines intact.

### Verizon Cellphones

This is not really an issue for device "Security" as we've defined it, but it's an issue for anonymity (talked about later in the "web-browsing" section), and it's device specific. If you are trying to use a cellphone in a semi-anonymous fashion on the Verizon network, you need to worry about an extra tracking token Verizon's network tacks on all your traffic. 

Risks:
  Only a problem for anonymity, not for security.

Alternatives:
 1. To opt out take a look (here)[http://clark.com/technology/how-opt-out-verizons-super-cookie-tracking/]
 1. If your area is covered, you could use a carrier who isn't doing something this shady in the first place.

## Likely not compromized systems
### Purism products (phones/laptops)
We're going to throw in a small plug for [Purism products](https://puri.sm/products/) (no we've no affiliation). As you can see by the above list, there are a lot of problems with most manufacturers. Consumers largely aren't aware of these issues in the first place and so there is little pressure to make better, more secure products. Buying from companies like Purism will likely get you a more secure system (for a price, to be sure), as well as help put pressure on other companies to do better.

## Getting Rid of Data / Destroying a Hard Drive

If you are using full disk encryption, and don't have the FBI or something after you, don't worry about it. 

If you aren't using full disk encryption though, you should seriously consider what is on your machine before ever letting it out of your hands. In that case the following sections may be important to you

### Data Erasure

Deleting files does not mean they are gone from your computer. It only means that you have told your computer they aren't there, and may be overwritten with other data. Until another program actually overwrites the space (something hard to determine), anybody with the right tools can recover the information.

Even after you overwrite the data the first time, it is still possible (though more difficult) to recover data. A state police lab can do this easily, as can some individuals. This is why there are programs on the internet which will write your drive to entirely zeros, or even random junk data to your drive over and over again for you. Running these over and over again will progressively decrease the odds that data can be recovered to the point of near impossibility (good enough for even most paranoid folks), but will not 100% guarantee it.

### Physical Destruction

At this point physically destroying the drives may be a good option. Just smashing the "drive" which stores the data makes getting the data harder. However, if you have [really attracted some attention to yourself](http://www.popularmechanics.com/technology/security/how-to/a8566/how-to-read-a-smashed-hard-drive-14877558/), you should know that the relevant pieces of data can be stored on extremely small pieces of the drive, so it can be difficult to make sure you have properly destroyed the drive. 

Corporations with serious data security concerns go through a fairly specific process. Best practice today is:
 1. Have the drive encrypted in the first place, just in case it goes missing.
 1. "Degauss" the drive. This means to run very strong magnets over it over and over, flipping the field back and forth. This is similar (but much faster) than writing lots of random data over it repeatedly.
 1. Powder the drive. Meaning to literally grind the drive in to dust.

This will always work, but most of us don't have a machine capable of powdering a hard-drive lying around. So lets talk about doing it by hand. There are two kinds of hard drives, and each have different relevant parts to destroy.

#### HDD: Hybrid Hard Drive (Old Kind)

The data is kept on a circular object called a platter. If you open the case, it is the large circular thing. Remove it (you can smash it to make it easier to remove, but that won't do it on its own). Watch out for the magnets, which are strong enough to break fingers if they become dislodged and rush together with you in the middle. Make sure you leave nothing connected to the center, as your data takes up extremely small amounts of space.

#### SSD: Solid State Drive (New Kind. Sometimes in desktops, almost always in laptops)

When you access a solid state hard drive's board, you will see a bunch of black computer chips which are likely symmetrically mounted. Your data is stored in those chips. You can pry the chips off the board with a Flathead screwdriver. Ideally you then smash these chips as well.

# Communication Security
## Email
We talked about the basic problems with email security (web-based or otherwise) in the "Basics" section. Lets talk about how we can make things better (at a cost).

### PGP
PGP (Pretty Good Privacy) bypasses all of this. The idea is simple. You encrypt the email on your computer, and the person you are sending to decrypts it on their computer. No-one in-between can see it, and no-one can decrypt the mesage but the person you are sending it too. This gives you very strong encryption and authentication.  
Here's the basic idea of how it works:

 1. You generate a PGP key, which consists of two large numbers one is "private" (don't tell it to anyone), the other is public (tell it to anyone you want).
 1. You publish the Public key.
 1. You're friend encrypts the message using your public key, and sends the message to you.
 1. You decrypt the messaging using your private key. 

You'll notice in our steps above that the person who is sending, and the one who is recieving need PGP software.

This document would get very long if we tried to write tutorials for every technology. Finding a good PGP tutorial online is pretty easy, just do a quick search. We will say though that ECC is believed to be the most secure right now... though not everyone you talk to may support it as it's newer. DSA is the next best. When it asks how many bits, make it as big as you can... 2048 is probably a minimum.

 * Windows (most machines): [https://www.deepdotweb.com/2013/11/11/pgp-tutorial-for-newbs-gpg4win/]
 * Apple: http://notes.jerzygangi.com/the-best-pgp-tutorial-for-mac-os-x-ever/
 * Linux: [https://help.ubuntu.com/community/GnuPrivacyGuardHowto]
 * Android (most smartphones): Generate the key on your computer, then use K9-mail
 * Apple phone: Generate the key on your computer. There are several options for an email app, here's one thought [http://pgpeverywhere.com/]

### Leaking to news sources (SecureDrop)
This is under Email because that's what you'd be temped to use... but there's a better option. One reason you might be reading this is if you have information, and are looking for how to leak it without someone tracking you down. The solution to this problem is called "SecureDrop". Here's how it works:

 1. Install TOR browser (mentioned later) or use Tails and run TOR browser from there.
 1. Using TOR browser Find a media outlet that supports SecureDrop. Here's an example, but I suggest you visit whatever media outlets securedrop page you choose ONLY via TOR [https://news.vice.com/securedrop/].
 1. Access the media outlets SecureDrop landing page e.g. [cxoqh6bd23xa6yiz.onion].
 1. Follow the instructions.

Since it's easy, you might as well do this from a coffee-shop as well, just to add one more layer of anonymity.

Risks:
  1. In the TOR section later, we talk about the weeknesses of TOR. TOR hidden endpoints (that weird .onion address), have been tracked down by the NSA/FBI... but it's very difficult and likely requires large amounts of repeated traffic, think nearly continuous transactions. Also, the sites that have been tracked down have usually been involved in trading millions of dollars of drugs, murders, etc. Tracking your bit of traffic down will be hard to impossible, and even if they do that there are still more layers protecting you.

Conclusion: This is the most secure/anonymous existing method to leak information.

### Re-mailers
A remailer will help you send an email without anyone knowing where it came from. If you can't use SecureDrop (described above) this is your next best option. Here's some info on remailers [https://www.cypherpunks.to/remailers/]

If you send an email to [remailer@cypherpunks.to] with the subject "remailer-help" you'll get an email back on how to use it.

## Realtime Chat
This is a common desire, and there are actually a LOT of tools out there to help you out. We'll talk about both the ones you probably use now, as well as options giving you better security.

### Normal Text Messaging
Cellphone type text messaging has a number of security flaws inherent in it's
design.

Risks:

 1. Cellphone companies can trivially log SMS, and probably do.
 1. Cellphone systems use extremely weak encryption (analogous to the rot13 example earlier), with no authentication. It's simple and cheap for an attacker on the same cell-tower to decrypt and listen using off-the-shelf hardware.
 1. The FBI or police are likely logging the messages *directly*. The FBI and police departments routinely use cell-site-simulators at rallies and protests now. These devices pretend to be the cell-phone-tower your cellphone would normally talk to. Your cellphone happily connects to this simulator, and the simulator thus gets your traffic, records it, and then forwards the traffic on to the normal phone network.

Conclusion: Functionally you get none of Authentication, encryption, or anonymity.

### Signal (cellphones)
Signal is a cellphone app designed to replace normal texting, but adding in strong encryption and authorization. So when you send a message you know it's going to the person you send it to, and only them. Playing a little buzzword bingo, it's open source, peer-reviewed, and [endorsed by Edward Snowden](https://www.youtube.com/watch?v=j_kieJ-Ng2Q). [Signal](https://whispersystems.org/) is an easy first step for anybody interested in basic security. You can install it directly from the app-store on virtually any phone.  You can also download signal through the designer website [here](https://whispersystems.org/).

Earlier I said it's authenticated, but there's a catch. Before you get a strong authentication guarantee you have to meet with the person you want to communicate with and use the "verify safety numbers" (in the conversation settings on the android version) feature. Basically this step ensures that the Signal knows that it's authenticating everything to the right person.

If you get a new phone, you will currently have to re-do key exchanges. This is an issue with Signal, not with the underlying technology.

Risks:

 1. You're still on a cellphone, so keep in mind device security.
 1. Signal, the cellphone company, and the police running their cell-site-simulator can still see you are talking to your friend, just not what you are saying.

Conclusion: Authentication, Encryption, but no anonymity.

### Threema (cellphones)

Threema is a secured messaging system which focuses on also granting anonymity and runs a full stack in-house in Switzerland, a very free country by internet standards. You don't sign up with any personal information, and you can only add people by learning their IDs. You can download their app from the app store or [their website](https://threema.ch/en).

We haven't researched this app in detail yet, so more details are needed

Risks:

 1. Note that it's actually "pseudonymous" not anonymous. The IDs are persistent, and thus someone can see that ID1 is talking to ID2, and ID1 talked to ID3 yesterday... they just don't know who ID1 and ID2 are.

Conclusion: Unknown authentication, unknown encryption, partial anonymity.

### Wickr (cellphones, computers)

Wickr is a secured messaging protocol where messages disappear after a period, like Snapchat except with privacy. Also like Snapchat, it can occasionally be a little fussy until you get use to it. You can download it in the app stores or [on their website.](https://www.wickr.com/personal)

We haven't researched this app in detail yet, so more details are needed

### Google/Facebook web-based chat
What about just using the web interface to Google "hangouts", or Facebook chat?

Risks:

 1. See browsing security. HTTPS isn't all it's cracked up to be (poor authentication)
 1. Your text is encrypted only to their server, then decrypted. It's re-encrypted to send to the person you are chatting with. So, your conversation can be seen by the corporation.
 1. Note that by default your conversation is also logged by Google, but you can turn this off by turning on "OTR"... Note that this OTR has nothing to do with the algorithm discussed later and just disables logging.
 1. A third party can see that you are talking, only Google can see who you are talking to.

Conclusion: Weak authentication, weak encryption, poor anonymity

### Facebook Messaging Phone app
Surprisingly, Facebook has added proper end-to-end encryption. This allows you to encrypt your messages such that Facebook can't read them. To use this though, you have to enable it every time you chat. 

Risks:

 1. Encryption is believed to be pretty solid
 1. Authentication is based on Facebook ID, so as long as you make sure that Facebook friend of yours is actually your friend, you should be good.
 1. It gives no anonymity guarantees
 1. It's on the phone, so watch that device security
 1. Facebook could change their app or server systems anytime, for example at the request of government entities.

Results: okay authentication, good encryption, no anonymity

### Pidgin/Adium + OTR (computers)
OTR (Off The Record) isn't actually a chat system, instead it's an algorithm that can be used on top of most existing chat systems. OTR is one of the very few examples of a communication system that supplies all
of encryption, authentication, and anonymity. Rather than being designed to make money, it was designed as a research product, and subsequently peer reviewed... so it's about as solid of a system as you'll find. Details here: [Cypherpunks](https://otr.cypherpunks.ca/). It's been reviewed by numerous security professionals and non-professionals alike, including a group of CMU undergrads who got curious one evening ;-) .

Okay, it's not a chat system, so how do you use it? The answer is:

 1. Install [Pidgin if you're using Windows or Linux](https://www.pidgin.im/) and [Adium if you have an apple machine](https://adium.im/). These are actually the same codebase, just named differently.
 1. Install The OTR plugin for that piece of software.  Here is [how you set up OTR on Adium](https://adium.im/help/pgs/AdvancedFeatures-OTREncryption.html). The Pidgin setup is a little bit more involved. [Windows has its own installer](https://otr.cypherpunks.ca/index.php#downloads) which you run separately. [Linux instructions](https://ssd.eff.org/en/module/how-use-otr-linux) vary by the version of Linux, but generally there is a separate package for pidgin with OTR already installed that is handled by your package manager (if you run Linux, you probably know what that means). 
 1. Get your friend to do the same.
 1. To get solid authentication, you have to verify that the key you get is actually associated with your friend.
 1. Chat with them using whatever chat system you like: AIM, MSN, ICQ, etc. 

This solution worked a lot better back when Facebook and Google used standard chat protocols (namely XMPP)... basically, when they played nice. Unfortunately they don't play nice anymore, so making this solution work with Facebook or Google chat can be problematic. Also, note that there is no cellphone solution listed, though you may be able to hunt one down, none are known at the time of this writing.

Risks:

 1. Honestly, this is as good as security gets. Open source, peer reviewed software with no corporation in the middle. It uses the best anonymity, authentication, and encryption algorithms available. We're down to device security.

Results: Everything you want security-wise

## Voice Chat
Many of the text chat systems support voice as well, and security is usually about
the same.

Cellphones, Facebook/google web interfaces all follow the same patterns. Pidgin/Adium don't do this very well.

## Video Chat
// TODO

## Web Browsing
Remember our 4 properties again:

 1. Authorization means viewing the website you were trying to view, rather than
   some other website.
 1. Encryption means no-one but you and the website knowing what you do on the
   website
 1. Anonymity means that no-one but you and the website know you even *visited*
   the website.
 1. Availability means the ability to get to a website

We talked mostly about #1 and #2 earlier, lets dive in to #3 and #4 now

### Improving Availability (and Authorization too)

Remember that I said that governments and some corporations can violate the authorization of HTTPS if they can intercept your traffic? That's an important if. There are methods to make that interception more difficult.

#### VPNs 

A VPN, or "Virtual Private Network", is essentially a computer based somewhere else and a secure tube to it. Most communications from your computer flow over this tube and out the other computer, as if your computer were where the VPN computer is.

There are two major reasons to use a VPN:

 1. To route around censorship or spying: If the internet is censored or monitored in your country (e.g. China for censorship, U.S. for spying), but not in some other country, you can get a VPN in the other country. Then you can use this remote computer's view to see whatever the internet looks like from the perspective of that computer. This will allow you to access sites not available in your country. 
 1. To secure your link to the internet: When on public WiFi (like a hotel or coffee shop), or other suspect wireless (See router information). You can use a VPN to make sure all traffic, over that part of the network at least, is encrypted and authenticated. Another example of this sort of use is if your internet provider is not trustworthy and is modifying traffic... such as making your online videos slow (Netflix/YouTube). 

For tech nerds: while you can rent a machine or VPS and set up your own VPN from scratch, it's an investment and it actually loses some anonymity gains a VPN might offer. If your goal is just to talk securely with your own server with strong encryption and authorization, this is a great option though. It does mean you can trust the provider though, assuming you trust your hosting provider.

For most people a better option is to rent a VPN. One apparently trustworthy and cheap option is [Private Internet Access](https://www.privateinternetaccess.com/). One advantage of using them is they have sites all over the world. You can just have it route traffic wherever it likes if your goal is #2 on my list above, but if it's #1 you can explicitly select a location. A good location to avoid spying and censorship is Iceland, as they have shown an interest in being a center for digital freedom. Note that PIA has simple setup directions for computers and phones of almost all types.

Risks:

 1. Internet providers, government agencies, etc. will still be able to see that you are sending data out of the country (if your VPN is out of country).
 1. If you use your own VPN they will be able to see who you are, if you use a heavily traffic public VPN you make tracking down who you are that much harder (since your traffic is mixed with everyone else's), but not impossible.
 1. DNS doesn't flow over the VPN without a lot of extra work. DNS has no authorization, and violating DNS authorization is a useful step in violating HTTPS authorization.
 1. The usual Browsing leaks are still an issue 

Results: Might help with anonymity. It makes redirecting your traffic a little harder, so it's a small help to authorization. Can be used to route outside your country so helps availability.

### Improving Anonymity

This is the hardest property to get while web browsing.

There are a lot of things against you. What you do on WiFi is visible to everyone using that WiFi. Additionally it's visible to the Internet provider (the company you pay for "internet", like Comcast or AT&T), and to lots of other corporations and government entities on it's way to the website.

Here are the major leaks to think about:

 1. DNS leak: When you visit a website like "www.google.com", your computer has to look up where on the internet that website is. To do this it uses DNS (Domain Name Service). Usually your machine asks the nearest router the question (like the WiFi access point you have at home). If that device doesn't know it passes the question on up the hierarchy, and eventually when someone has the answer they respond, that DNS server responds in kind, etc. until the nearest router tells your machine the answer. Everyone I spoke of above, can see this request and answer.
 1. Your "Internet Address": When you get information from a website, you send information to the website about how to send information back to your computer... like a return address. Everyone I just spoke of can see this return address, even if you are using HTTPS.
 1. Logins: Now lets say you are using a website. Many websites require you to log in. This is a unique identifier that website can and will associate with everything you do on their website as they log it. As mentioned earlier, logs are often handed over to government agencies.
 1. Cookies: Many websites drop a "cookie" on your machine when you visit the website. This way if you visit it again they can tell it's the same person. Functionally this is just like a login for them, except you don't have to log in. 
 1. Advertising: Advertising often has trick code in it involving cookies or more subtle things to help uniquely identify you. These are particularly problematic as the same advertising company advertises all over the web, so the identifiers they assign to you aren't just for one website, but for sites all over the web.
 1. Browser identification: To help decide what information to show you, your machine tells websites a lot of information about your machine: what type of machine it is, what type of browser it is, all the plugins you have installed, the dimensions of your browser window, etc. For those who think they know how to work around this, a lot of information is leaked via JavaScript rather than user-agent information
 1. Browser Leaks: One website you have loaded can tell what *other* websites you have open in the same browser. Prominent examples include Facebook, and most songs lyrics sites.

Looking at that list, it becomes clear we have our work cut out for us. It's also pretty obvious that doing a perfect job is nearly impossible, so it's a matter of trying to do the best we can.

#### Don't log in to things
If you are trying to be anonymous... don't log in to things unless you have to.

Whatever you do do NOT log in to Facebook, and then browse something you want to be anonymous. Before doing something anonymous, wipe all your browser data (cookies, etc.), close your browser, and open it again. Even better, use a separate browser (like TOR Browser) only for your anonymous work, and only log in to anything on it when you HAVE to as part of that semi-anonymous/pseudonymous work.

Configuring your browser to dump all this information every time you close it makes this process easier. Chrome seems to have removed this feature, but Firefox still has it.

#### Disable Cookies
In your browser settings you can disable cookies from all hosts, or just remove hosts. Note that this will break many websites, so you may want to do this only in the browser you use for your anonymous/pseudonymous work.

#### Disable most CA-certs
For tech people only, This is pretty advanced, and is a pain to maintain, but if you really want to get paranoid this is a great idea. If you don't understand this, don't worry, just move on.

The weakness in HTTPS relates to the root certificates built in to the browser. Chances are you don't need them all, especially for your anonymous/pseudonymous work. So, you can disable them. One good method is to disable them ALL. Then when you visit a website you need and HTTPS fails to authenticate, look up the cert information for that site. Go in and find that root cert, and enable it again.

For each root-cert you enable, you are allowing the owner of that root-cert to middle-man your HTTPS sessions, but at least this lets you control who that is. You may want to look up various root certs and associated companies to see what government they are associated with, Verisign is the U.S. for example.

#### Use TOR
TOR stands for "The Onion Router". [TOR]( https://www.torproject.org/) is software and accompanying network used to help achieve anonymity on the internet, most often used for web browsing.

The Weakness of a VPN, as noted above, is that the VPN provider knows exactly who you are, and can look at your traffic. TOR attempts to fix this flaw. Imagine you use one VPN. Then, set up a VPN to another machine, and another.  When your traffic leaves your machine it's wrapped in 3 layers of encryption.  The first machine strips away 1 layer, leaving 2 more. second VPN another layer, and the third VPN yet another finally sending your traffic out on to the open internet. This is essentially how TOR works. The idea is that the VPN machine knows who you are, but can't see your traffic. The last can see your traffic, but only knows the machine it's talking to, not who you are.

Unsurprisingly, with your traffic bouncing all over the internet and getting encrypted and decrypted over and over again, your browsing experience is going to feel slow compared to normal. For this reason, while you could use it all of the time to make the fact that you are using it less suspicious, it's usually used just when you are doing something where you need it.

To use TOR we recommend using TOR browser, as it just works. Getting clean switching to turn it on and off, dealing with DNS leaks, and dealing other privacy leaks can be difficult and takes a fair bit of time, technical knowledge, and skill. Feel free to go it on your own, but be aware that it's easy to screw up and leak something. If what you are doing matters, you'll want to spend some time being sure you got it right.

Risks:

 1. Government agencies are able to track down TOR communications, and have staged several [major crackdowns on illegal activity using TOR](https://www.wired.com/2014/11/operation-onymous-dark-web-arrests/). It is widely believed that the U.S. NSA is running a large portion of the nodes. TOR depends on that first and last machine not colluding, if both are machines run by the same people you lose.
 1. You're still vulnerable to the usual DNS leaks, JavaScript browser identification techniques, cookies, etc. The devil's in the details... see TOR Browser below.

Results: Similar to a VPN. It helps a lot more with anonymity but is also a little more likely to make you a target.

##### TOR Browser
The Tor Browser is The easiest solution for using TOR. Read more [here](https://www.torproject.org/projects/torbrowser.html.en).

TOR browser is like any other web browser. It's the bit of software you load to view the internet, filling the same role as Internet Explorer (default on windows), Firefox (default on Linux), Chrome, etc. You're old browser will still be present. How to install it and run it depends on your system, see the website for details. In all cases though, to use TOR you'll want to run the TOR Browser, rather than whatever you usually use to browse the web. To browse the web normally when you aren't worried about anonymity and all that, you can still load up your normal default web browser.

Note that the TOR Browser solves the DNS request leak for you, and even helps a bit with browser identification. In short, if you don't know what you are doing it "just works". Install it, and use it, preferably without configuring ANYTHING. That's about the best anonymity you can get (except maybe tails below).

##### Tails
We mentioned tails earlier... Tails is a full bootable OS image with TOR Browser already set up, and solves even more possible issues for you. If you are considering using TOR Browser, this may be good option.

# Maintaining Information Availability 
We've talked already about how to get to websites that might be blocked where you are... but what about websites being taken down entirely, and the data simply disappearing from the internet? This is where "Information Availability" becomes an issue.

Government removal of information from the internet is becoming increasingly easy. The United States government already has the infrastructure and authority to [seize domain names](https://www.justice.gov/usao-sc/pr/federal-court-orders-seizure-67-website-domains-involved-smuggling-and-selling-misbranded), effectively removing sites from the Internet. 

## Help host it (Tech savvy only)
In many cases sites may get taken down by a government due to being "illegal" in that country for some reason. If that data is legal in *your* country, you may be able to download or copy that information, and put it up yourself.

Before doing this sort of thing, check your local laws. Consider consulting a lawyer, etc. Make sure that you aren't putting yourself in more danger than you are comfortable with. 

## Decentralized storage networks
Hosting in another country can definitely help, but the site may still be blocked to people who you'd like to have access to it, or possibly it's not possible to host it anywhere, what else can we do?

The normal solution to this is to use a decentralized information network. Bit Torrent is one of the protocols often used to do this. This solves the problem of any one central point of failure. The downside of such distributed networks is trust. Anybody can put a torrent up, so you don't know if it is trustworthy, it might actually be malware.

Unfortunately, knowing if you can trust a file you download is a problem we have everywhere on the internet. Malicious people can switch out files on your network. This is why we also have systems to verify that a file has not been tampered with in transit, and that it comes from where you think it comes from.

### Torrenting
//TODO

### Signatures and Checksums
//TODO

# Other Legal Issues (though not legal advice, we are not lawyers)

## U.S. Customs and border patrol
When passing through U.S. customs it's probably smart to assume all your devices may be seized and searched. Customs claims that since they can search your luggage, they can also search your devices. They extend this to include data stored in the cloud which your device has access to. Though it's not commonly done, they can and do take devices and image them, or they can hold you indefinitely until you agree to unlock a device so they can access the data. For this reason burner phones and the like may be your best bet when crossing the U.S. border.

##  Passwords not necessarily protected by U.S. 5'th amendment
It's currently unclear whether giving up a password is protected by 5'th amendment rights. There is at least one case where someone has been put in jail for over 2 years (as of now) for not giving up a password to data encrypted on his computer's hard drive (believed to be child pornography in this case).

# How can I help?
## Running a TOR Node

Running a TOR middle node is helpful, and fairly low risk. If you have bandwidth to spare it's not all that hard to set up, and it's easy to set limits on how much bandwidth it is allowed to use. 

If you are braver, and willing to get involved in legal battles (depending on your country, some may have fewer issues) you can do a HUGE service to internet freedom by running a TOR Exit node. A major problem with TOR is many exit nodes are run by the government, the more that are not, the better for internet freedom. An Exit node is the place where the activity of people using TOR finally gets the last layer of encryption removed, and it becomes available to the government and others to watch.

Many users of TOR are up to nefarious deeds, and as a result much traffic flowing out of TOR (your Exit node if you run one) is nefarious in nature, and you will get blamed for it. This is the nature of freedom, to protect people from censorship, we also protect bad actors activities as well.

If you are willing to take this on here is [Noisebridge's guide on responding to federal inquiries about their tor exit node](https://www.noisebridge.net/wiki/Noisebridge_Tor/FBI). 

Please seriously consider [running a Tor exit node](https://blog.torproject.org/blog/tips-running-exit-node), particularly if you live in a country with stronger civil liberties. 

## Downloading and Storing Activist Information for Offline Distribution

If the information is stored places besides the internet, internet censorship can't affect it.

Similarly many people don't have easy access to information on the web, or don't know it's out there. Help spread the good word. The ACLU is a good place to start. For example, here is their [protest guide](https://www.aclu.org/know-your-rights/what-do-if-your-rights-are-violated-demonstration-or-protest)

## Help improve this document

Comment on git, or email mbrewer@smalladventures.net.

At this point virtually all feedback is welcome. Improvements, corrections, confusions, etc.

