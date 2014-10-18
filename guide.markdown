<h1>Privacy Guide for Activists with Haters</h1>
In light of the gamergate fiasco, we realized that most of the targeted individuals had their private information trivially publically online. This guide is meant to help people take basic steps required to protect their online privacy, hopefully reducing the number of crazies who threaten to show up at your house.

We do not believe that leaving your information online means you deserve harassment, we simply wish to arm people who want to speak up with all the defensive tools available.

This guide is not an anti-government-survelience document, as it only helps you make your information private and does not remove it.

<h2>Hiding Your Whois Data</h2>
This one should be easy, but it is the number one privacy failure we found when checking information of indviduals who have previously been harassed.

When you register a domain, you fill out contact information which by default is _public_. You can trivially check what information is public in any Linux/OSX terminal

    whois www.example.com

If you're not a machine which supports the whois command you can use one of the many [online tools](http://www.whois.net/) to check your the wholis records.

If your personal information is available, we advise you to take one of the following actions:
* Purchase a privacy plan from your domain from your registrar
* Purchase a domain by proxy plan and have them handle your domains
* Migrate to a registrar which provides free domain name privacy (namecheap gives it for free your first year)

Whois data isn't generally publicaly cached, so once you fix this you should be good to go!

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

* Twitter and Facebook remove photo exif data by default, but twitpic does not. Either disable locations on twitpic or don't use it.
* Flickr permits you to upload information with EXIF data. Consider disabling it when you post from sensitive locations.
* If you have an anonymous persona strip all EXIF data from all photos you upload. A device ID can link your public and private personas.
* Imgur automatically strips all information, so when in doubt, they are very safe and awesome!

<h2>About</h2>

This privacy guide is made by [Katy Levinson](https://twitter.com/katylevinson) and a privacy-concerned friend. It was debugged with love by Katy's coworkers at [Crooked Tree Studios](http://throwtrucks.com/) 

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/), though we'd prefer that you just submit patches to this gist. If you want to give us money for this public service, [give it to the EFF instead](https://supporters.eff.org/donate).