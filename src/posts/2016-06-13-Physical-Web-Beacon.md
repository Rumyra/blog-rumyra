---
title: I got a Physical Web Beacon!
date: '2016-06-13'
category: craft-code
tags:
- beacon
- bluetooth
- ble
- physical web
status: published
---

<figure>
  <img src="media/beacon.jpg" />
</figure>

Yay

[Dan](https://twitter.com/dan_jenkins) gave me a beacon! (Well [Paul](https://twitter.com/Paul_Kinlan) gave him some beacons and then he gave me one, so thanks both).

Super hyped about this. I managed to get one through work and then the wonderful [Terence](https://twitter.com/edent) took it back and [hacked a la Terence stylee](https://shkspr.mobi/blog/2016/02/inside-a-physical-web-ble-beacon/) (he found out some cool things, I’m not bitter).

But this one is my very own. However looking on [the Google Physical website](https://google.github.io/physical-web/), or doing a search, there’s no simple instructions to just change a URL on a beacon, so here’s some things I found out whilst doing it:

READMORE

All I want to do is alter the URL which is being emitted by the device, that’s it, no fuss, simples (well mostly)…

- You need an app to do this. There is a [web app](http://cf.physical-web.org/) if you’re on Chromebook (the Bluetooth Web API isn’t advanced enough on other versions of Chrome yet to work on other platforms). If you’re running android [this app](https://play.google.com/store/apps/details?id=physical_web.org.physicalweb&hl=en_GB) comes recommended. My real caveat was I’m running an iPhone 6S and a Macbook Air OSX 10.11… trying to find an app that would link with my Beacon and update was the trickiest part. As I was given my beacon I don’t have a default manufacturer or app.

- Make sure Bluetooth is switched on.

- Switch your beacon on and check it. I have the latest version of Chrome installed on my phone, so if I check my notifications under *'Chrome'* it says _'Scanning for physical web devices'_ and then pops up with the URL set on the beacon, with an easy clickable link. Phew well that’s much easier than typing in a url! It also means your beacon is working. (If you don't have notifications switched on for Chrome [check out this video](https://docs.pushmote.com/docs/how-to-enable-chromes-physical-web-extension-on-the-ios))

<figure class="media-feature">
  <img src="media/chromeNoti.jpg" />
</figure>

- I want to change this url. I’m going to be carrying around the device in my handbag, so I’ll put my blog on it. Something to note is new physical web devices don’t accept non https urls.  Now here’s the deal, apps I tried that *didn’t* work are: [Beacon Tools](https://itunes.apple.com/us/app/beacon-tools/id1094371356?mt=8), [eBeacon](https://itunes.apple.com/us/app/ebeacon-ibeacon-eddystone/id730279939?mt=8) and [MyBeacon](https://itunes.apple.com/us/app/my-beacon-best-beacon-manager/id850255614?mt=8) Thank you to [Hemanth](https://twitter.com/gnumanth), [Dan](https://twitter.com/dan_jenkins), [Jean-François](https://twitter.com/jefbinomed) and [Francois](https://github.com/beaufortfrancois) for they’re advice as I finally installed [Physical Web app](https://itunes.apple.com/fr/app/physical-web/id927653608?mt=8) and sure enough managed to change the url.

There’s loads more to be said about configuring beacons, physical web and the web bluetooth api. If you get stuck I found the afore mentioned peeps very helpful.

Now to try and hack the hex data…