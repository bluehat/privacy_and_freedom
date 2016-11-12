# A Citizen's Guide to Digital Freedoms

# 0: Why
We're about to hand the architecture for a surveillance police state over to new leadership. Some of Trump's language around free speech and free press has been troubling. This seems like an excellent time for us to evaluate the state of the internet, and education on how technology can be used to protect citizen's civil liberties.

The goal of this guide is to create lesson plans which nontechnical people can then use to run classes for groups of nontechnical people. 

Calling this a rough draft would be generous. Help is appreciated, especially from: 
 1. More technical people to provide content.
 1. Less technical people to explain what areas are not clear.
 1. People who can make illustrations and diagrams to make complicated concepts simple
 1. People with teaching experience to help figure out how to break this into a course people can teach each other

This guide will not make you safe. It will increase your chances of safety.

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), though we'd prefer that you just submit patches to [this gist](https://gist.github.com/bluehat/76a07a5d25f038a89f3b99c54a9a94a9). If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate).

# 1: Communication Privacy

## 1.0: Security, Authentication, and Encryption

### Security
Security means that your messages can't be understood by anybody except the party you are sending them to.

### Authentication
Authentication means the person who is getting your messages is the person you want to have your messages. Most security technology will successfully auto-establish a secure connection on its own, but you need to take extra precautions to make sure you are talking to the correct person on the secure channel.

### Communication Encryption
We are working with public key cryptopgraphy.

Public key cryptography is like an old-time wax seal people used to seal letters, except it actually works.

You can [more detailed explanations of public key cryptography](https://blog.vrypan.net/2013/08/28/public-key-cryptography-for-non-geeks/) but for our purposes just remember you have two things called keys, but which are actually large (hundred+ digit) numbers. One is called your public key, and one is callled your private key. 

Your private key is the equivalent of the stamp which makes your wax seal: it is used to sign documents. If anybody ever steals the stamp you use to make little wax seals, you are in deep water. **You must protect your private key.**

Your public key is the address of a mailbox which only you can open.

The keys are inherrently linked. They are set up so that your private key (thing which makes your wax seals) is the only thing which can open your mailbox, and your public key (the address of your mailbox) can be used to verify the authenticity of the wax seal on your letters.

The one thing the math can not solve is making sure you do the setup work with the right person. Imagine you and your friend have never sent messeges each way before. The first thing you'd have to do is tell your friend where your mailbox is and show them how to verify your wax seal's authenticity. If you do this over the internet, you're basically sending a courier nobody's met before who is just going to show up and claim to be working for you. 

Your friend can't trust that courier. A bad person could catch the courier at a crossroads and kill them. Then they could steal your courier's uniform, send their own courier, and give your friend the address of a mailbox they claim belongs to you, but really belongs to the bad guy. If they did this to both of you all the messages on both sides would be delivered instead to the bad person. If the bad person was diligant about forwarding the messages with their setup, you and your friend would never know there was somebody in the middle watching everything you do. This is why mailbox address / public key exchanges are normally done in person, or by a method which is built off a network of people verifying keys in person. In the security community, they are often added to people's business cards.

This is why you need to worry about both security and authentication. The technology will make you secure, but you will always need to take precautions to make sure the person you think you are speaking with is the one you intended to speak with.

**Short Version: Your private key is very secret: way more secret even than your social security number ought to be. Your public key is something you can tell to whoever you want, like a phone number. Don't trust keys if you aren't sure they belong to your friends**

## 1.1: Signal / Securing your SMS

Open source, peer-reviewed, and [endorsed by Edward Snowden](https://www.youtube.com/watch?v=j_kieJ-Ng2Q), [Signal](https://whispersystems.org/) is an easy first step for anybody interested in basic security. It has been on both the Android and iOS app stores for many years, and works with most phone OS versions.

Remember that until you have also authenticated your contacts using "verify safety numbers" (in the conversation settings on the android version) you can be sure whoever is getting your information gets it securely, but you will not have a guarantee that the person who is getting it is the person you want to get it.

Outside actors will be able to determine who you communicated with and when, but not what you said.

If your phone is hacked by something else (like maybe you downloading shady apps) your texts will still be readable by whoever has hacked your phone. That person could also gain access to your private keys.

If you get a new phone, you will currently have to re-do key exchanges. This is an issue with Signal, not with the underlying technology.

You can download signal on the app store or [through their website](https://whispersystems.org/).

## 1.2: Adding Encryption to Existing Messaging Protocols

### OTR for Adium

### XMPP

## 1.3 Secured Messaging Protocols

## 1.4: Encrypting Your Email

# 2: Anti-Censorship

## 2.0: Censorship Mechanics

Governments such as China outright block many websites outside their country. Governments like Pakistan are intercepting all outbound traffic before it leaves the country so they can watch it.

These measures are meant to help you keep access to content which a dictatorship does not want you to see.

## 2.1: VPNs 

A VPN, or Virtual Private Network, is essentially a computer based somewhere else. You make a secure tube from your internet to that other placem and look through it. You can use this computer to see whatever the internet looks like from the perspective of that computer. This means that if a website is blocked in your country, you can use a VPN to "get to the internet" in another country, and then see the website.

They are commonly used now to get around traffic shaping measures by your ISP (Internet Service Provider: aka Comcast etc). ISPs illegally throttle services like Netflix all the time, so opening a VPN to a colo means that they can't really traffic shape your encrypted data, they can only turn the speed up and down monolithically. VPNs are also used to make working on unsecured coffee shop wifi reasonable, and can be used to sidestep snooping by non-government actors, such as your school or workplace.

With a VPN, outside actors will still be able to see that you are sending data out of the country. They will be able to tell who you are unless you somehow make it incredibly difficult for them to tell what computer is connecting to the VPN. If the VPN is compromised, outside actors will be able to see what you look at, and possibly change what you are looking at.

This is why you want the other end of your VPN to come out in a place not controlled by whoever you are concerned is spying on you.

To set up a VPN, you will need to get an endpoint (normally a rented machine in a data center) and to configure your computer so all traffic goes through that endpoint. We are working to figure out easy ways to make this technology accessible to less technical people.

Iceland has shown an interest in being a center for digital freedom. Further research on the best VPN endpoints is appreciated, but for now, Iceland is advised for your endpoint.

## 2.2: Tor

# 3: Information Distribution, Verification, and Storage

# 3.0: Distribution and Protection Needs

### Known Compromised Systems
Windows 10's EULA stipulates that information from your machine can be taken for government use. This is why there will be a lesson in installing Linux.

## 3.1: Torrenting

## 3.2: Signatures and Checksums

## 3.3: Full Disk Encryption

## 3.4: Destroying a Hard Drive

# 4: Anonymity

## 4.0: Need

## 4.1: Remailers

## 4.2: Your IP Address

## 4.3: What Is a Clean Computer?

# 5: Legal 

## 5.0 Description

## 5.1 No Fingerprint Readers to Unlock Things

# 6: Contributing to Internet Freedom

## 6.0: Explanation

## 6.1: Running a Tor Exit Node
