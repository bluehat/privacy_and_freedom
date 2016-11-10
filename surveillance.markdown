# 0: Why
We're about to hand the architecture for a surveillance police state over to new leadership. Some of Trump's language around free speech and free press has been troubling. This seems like an excellent time for us to evaluate the state of the internet, and education on how technology can be used to protect citizen's civil liberties.

The goal of this guide is to create lesson plans which nontechnical people can then use to run classes for groups of nontechnical people. 

Calling this a rough draft would be generous. Help is appreciated, especially from 
1. More technical people to provide content.
1. Less technical people to explain what areas are not clear.
1. People who can make illustrations and diagrams to make complicated concepts simple
1. People with teaching experience to help figure out how to break this into a course people can teach each other

This guide will not make you safe. It will increase your chances of safety.

# 1: Communication Privacy

## 0.1: Security, Authentication, and Encryption

### Security
Security means that your messages can't be understood by anybody except the party you are sending them to.

### Authentication
Authentication means the person who is getting your messages is the person you want to have your messages. Most security technology will successfully auto-establish a secure connection on its own, but you need to take extra precautions to make sure you are talking to the correct person on the secure channel.

### Communication Encryption
We are working with public-private key encryption.

Key-based encryption is like an old-time wax seal people used to seal letters, except it actually works.

Encryption works by making things hard for a computer to read. This means that we had to figure out a way to make data look random, while also having a way to open it, without anybody else being able to calculate how to open it.

For this, we needed a kind of math computers are bad at.

Computers are bad at guessing prime numbers.

How this works is you get two big (several hundred digit long) numbers. One (your private key) is used to sign stuff and prove you wrote it, and the other (your public key) functions as a sort of inbox. You can use your private key and somebody else's public key to make a message only they can read, and that they know you sent.

Getting somebody else's public key is hard. If your key is sent by the internet, somebody in the middle can switch out the key you are suppose to get with one the bad person can read. Normally key exchange is done in person, or by a method which is built off a network of people verifying keys in person.

This is why you need to worry about both security and authentication. The technology will make you secure, but you will always need to take precautions to make sure the person you think you are speaking with is the one you intended to speak with.

## 1.1: Signal / Securing your SMS

Open source, peer-reviewed, and [endorsed by Edward Snowden](https://www.youtube.com/watch?v=j_kieJ-Ng2Q), [https://whispersystems.org/](Signal) is an easy first step for anybody interested in basic security. It has been on both the Android and iOS app stores for many years, and works with most phone OS versions.

Remember that until you have also authenticated your contacts using "verify safety numbers" (in the conversation settings on the android version) you can be sure whoever is getting your information gets it securely, but you will not have a guarantee that the person who is getting it is the person you want to get it.

Outside actors will be able to determine who you communicated with and when, but not what you said.

If your phone is hacked by something else (like maybe you downloading shady apps) your texts will still be readable by whoever has hacked your phone.

If you get a new phone, you will currently have to re-do key exchanges. This is an issue with Signal, not with the underlying technology.

You can download signal on the app store or [through their website](https://whispersystems.org/).

## 1.2: Adding Encryption to Existing Messaging Protocols

## 1.3: Encrypting Your Email

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

# 3 Information Distribution, Verification, and Storage

## 3.0 Distribution and Protection Needs

## 3.1 Torrenting

## 3.2 Signatures and Checksums

## 3.3 Full Disk Encryption
