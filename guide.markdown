<h1>Privacy Guide for Activists with Haters</h1>
In light of the gamergate fiasco, we realized that most of the targeted individuals had their private information trivially publicly online. This guide is meant to help people take basic steps required to protect their online privacy, hopefully reducing the number of crazies who threaten to show up at your house.

We do not believe that leaving your information online means you deserve harassment, we simply wish to arm people who want to speak up with all the defensive tools available.

This guide is not an anti-government-surveillance document, as it only helps you make your information private and does not remove it.

<h2>Hiding Your Whois Data</h2>
This one should be easy, but it is the number one privacy failure we found when checking information of individuals who have previously been harassed.

When you register a domain, you fill out contact information which by default is _public_. You can trivially check what information is public in any Linux/OSX terminal

    whois example.com

If you're not a machine which supports the whois command you can use one of the many [online tools](http://www.whois.net/) to check your the whois records.

If your personal information is available, we advise you to take one of the following actions:
* Purchase WhoisGuard for your domain from your registrar
* Purchase a domain by proxy plan and have them handle your domains
* Migrate to a registrar which provides free domain name privacy (namecheap gives it for free your first year)

Whois data isn't generally publicly cached, so once you fix this you should be good to go! It sometimes technically can be stored by certain services behind a paywall.

<h3>Advanced Whois Chaos</h3>
If your information is on your whois but out of date, put some of it through [reverse whois tools](http://www.expertusability.com/reverse-whois-search/). A matching phone number or email address can be used to find other domains registered with that information, and those records might be current.

<h2>Removing location data</h2>
While most activists are very good about this, no guide would be complete without it!

* [Disabling web location and removing your old location data on Twitter](https://support.twitter.com/articles/122236#)
* [Disabling mobile location on mobile devices](https://support.twitter.com/articles/118492-using-the-location-feature-on-mobile-devices#)
* [Disable location services on iOS](http://support.apple.com/kb/ht5594)
* Unfortunately, due to the way android phones are made, the camera app is normally different for each manufacturer, and so you will have to look up directions specific to your phone's make.

<h2>Removing EXIF data</h2>
EXIF data is a variety of information the device which captures your photo stores and uploads with your photo. If this device contains a GPS chip (like almost all cellphones do) the location where the photo was taken can be determined. [The EFF has a longer explanation](https://www.eff.org/deeplinks/2012/04/picture-worth-thousand-words-including-your-location) if you're curious.

* Twitter, Facebook and Tumblr remove sensitive photo EXIF data by default, but not all services do. 
* If you'd like to see what EXIF information a  site shows, take the URL of an image uploaded there and put it in [this website](http://exifdata.com/).
* Flickr permits you to upload information with EXIF data. Consider disabling it when you post from sensitive locations.
* If you have an anonymous persona, strip all EXIF data from all photos you upload. A device ID can link your public and private personas.
* Imgur automatically strips all sensitive information, so when in doubt, they are safe and awesome!

<h2>Searching by Images</h2>
If you recycle the same profile images over and over, you may be surprised what shows up if you [search by your profile image](http://www.google.com/insidesearch/features/images/searchbyimage.html).

<h2>Miscellaneous</h2>
* Don't hotlink images directly from Facebook unless you're OK with everybody knowing your Facebook profile.
* If you discuss your partner(s) or housemates publicly, remember to make sure they follow this guide too.

<h1>Make your accounts harder to steal!</h1>
<h2>2 Factor Authentication</h2>
We're sure you've been lectured on password security, and while your habits are probably terrible, we're going to focus today instead on 2-factor auth. 2-factor auth requires somebody to know your password _and_ have your phone or another physical device (or at least control over it). 

You're encouraged to enable 2-factor authentication on everything, but _prioritize accounts where password resets are sent_.

Here is an [amazing website with directions on how to do 2-factor auth on everything ever](https://twofactorauth.org/).

<h2>Update where password resets go</h2>
Check through your old accounts. Do you still own the old @hotmail.com where you registered your twitter handle 7 years ago? If you don't, somebody can register that name and take your password reset! Make sure your account recovery options go to a safe location. You can as many postmortem security reports you need to to get the picture: <b>this is the most common way somebody gets control of your online persona.</b> First they take the account where your main account (probably your gmail) goes to, they reset that password, then they login to your main account (probably your gmail) and the go to town.

<h2>Proper unique passwords</h2>
Remember how you thought your terrible habits would never come back to bite you? If you're reading this, you are obviously reconsidering that stance.

Convincing you to be an adult overnight is probably a lost cause, so install a password manager like [KeePass](http://keepass.whinfo/) or [LastPass](https://lastpass.com/).

Whenever possible, set up and use ssh keys instead of passwords.

<h1>Disaster Response</h1>
So you now have the internet's full attention. What precautions can you take to minimize damage? These measures are not for daily use as they are rather inconvenient, but more of a disaster response plan if, for example, your haters get out of hand enough to merit national television reports.

<h2>Freeze your credit</h2>
You can place a freeze on your credit, thereby preventing people from taking out new debts or credit cards in your name. You will need to freeze your credit with each of the 3 major credit burearus: [Experian](http://www.experian.com/consumer/security_freeze.html), [Transunion](http://www.transunion.com/securityfreeze) and [Equifax](https://www.freeze.equifax.com/Freeze/jsp/SFF_PersonalIDInfo.jsp) Please note: this is a pretty dramatic step. You should read about what it means to freeze your credit and consider the ramifications before doing it. You will also inconvenience yourself significantly if you'd like to take out any new loans or credit cards because you can't do that when you freeze your credit.

<h2>Disable all remote wipe settings</h2>
Your phone, tablets, and computers generally have settings to remove all of your data using only an internet connection. You normally enable these things because you believe your posessions are more likely to be stolen than the internet is to come hunting for you. When that calculation changes, it is time to disable any settings which permit remote wipes. [Apple products are notoriously sensitive to this issue.](http://www.emptyage.com/post/28679875595/yes-i-was-hacked-hard)

<h1>The Bad News</h1>
* If you own property, your address is a matter of public record. Sometimes you have to go to the office or call them to get it, but it can be legally obtained
* If you are registered to vote, your contact information can be accessed by any Super-PAC in most states. Becoming one costs about $300 and the records cost $15 to obtain
* Utility bills in your name, while they are not suppose to be something you can trace, often can be traced

<h2>What you can do</h2>
* Use a fake last name
* Petition your government to make citizen privacy a priority

<h1>About</h1>

This privacy guide is made by [Katy Levinson](https://twitter.com/katylevinson) and a privacy-concerned friend. It was debugged with love by Katy's coworkers at [Crooked Tree Studios](http://throwtrucks.com/), [Cliff Jolly](https://twitter.com/expiredpopsicle) and [Chris Meyer](twitter.com/cygnil).

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), though we'd prefer that you just submit patches to [this gist](https://gist.github.com/bluehat/354432b82650d0a722ed). If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate).