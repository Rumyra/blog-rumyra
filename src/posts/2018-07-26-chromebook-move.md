---
layout: post.html
title: "Moving to a Chromebook"
date:   2018-07-26
category: craft-code
tags:
- chromebook
- laptop
- hardware
image: media/chromebook.jpg
summary: "The move from a mac to a chromebook, and how that all went"
---

So here's the deal. The macbook broke, it broke a long time ago, possibly January. The space bar just stopped working, I mean the keyboard was a mess anyway, but this time :rolling_eyes:

I took extreme action and popped it off and sticky taped it back on, with a new _improved_ Ruth Crafted Button™

Problem. Solved.

Anyway, without going on a rant about Apple turning a blind eye, I was in no position to afford repairs. The _Genius'_ were no help and I had not budgeted for a new laptop for at least another 12-18 months. I expect Apple hardware to last a good 24-36 months, really. I dunno maybe I'm optimistic.

People came to my aid. Which was amazing. I was offered a pretty hefty discount on a Google Pixelbook. This is Google's own top of the range Chromebook. I could not refuse. After a battle with customs because the discount was only only valid in the States, it finally arrived on my doorstep last week.

Holy baps!

For those of you that are slamming mac keyboards as if your life depended on winning that game of wack-a-mole, revert, run, get the crap out! WORKING KEYBOARDS ARE JOYOUS. So so joyous.

### Some setup stuff

The first thing, and possibly the thing with the least amount of up to date information out there, was enabling Crostini. This runs Linux in a container on the Chromebook, something you pretty much want straight away after spending 15 minutes on it.

I have the most recent Pixel, the 256GB version. Here's what you do.

- Go to settings.
- Click on the hamburger menu (top left) - right at the bottom it says 'About Chrome OS'
- Open this and there's an option to put your machine into dev mode
- It'll restart and you'll be in dev mode - this is much like running Canary over Chrome and possibly turning on a couple of flags. It may crash, but what the hell you'll have Linux capabilities :)
- Now you can go back into Settings and in regular settings there's a 'Linux apps' option. Turn this on. It'll install Linux.

Once this is complete you'll have a terminal open for you. Perfect

Now you have to remember all those terminal commands you never use because you've been installing .dmg files for like ever!

`apt-get` is the biggy. I found [this link to be really helpful](https://www.howtogeek.com/63997/how-to-install-programs-in-ubuntu-in-the-command-line/). My main aim was to set it up so I could develop on it. I really only build things on node now and I will be running my mac alongside this machine for Adobe Creative Suite reasons (I have an old purchased copy), so I could be pretty minimal about my approach. Should I have to cope with an old ruby build for instance (or a new one) I'll just switch to the mac.

I use Sublime as my editor :scream: Please I run a MacBook, a book - not a pro. It just didn't handle vscode and there was no real estate with the 12" screen size. So I tried and I am fine with Sublime.

This installed perfectly well. There's some descrepencies with screen resolution when running Linux applications on Chromebooks. It's apparent in Sublime, but there's also a couple of settings you can play with `dpi_scale` and `ui_scale`. I set my `ui_scale` to 1.6 and it's fine.

I also revised my vim commands and know now I am running Debian v 9.4 Stretch (command for this is `lsb_release -a` btw). Useful information at these times.

One other thing that stumbled me was serving an app within the Debian container and accessing it from regular Chrome on ChromeOS (and if you are reading this with a haughty taughty _how do you not know this Ruth_, remember some of us hold other knowledge :rolling_eyes_right:).

What you are looking for is `ip address`; `ifconfig` is depreciated. Bang that in your terminal. The ip of your container is the one after `inet`. Shout out to my safe place [JSOxford](https://jsoxford.com/) for this one. Replace localhost with that (remember your port) and you're O K. Also if anyone knows of a better way of doing this lmk and I'll update, I saw some threads talking about using `dev.local` or such things in place of this.

Phew :sweat_face: this also actually took me a million years, so I am just gonna run and wash, brb.

Pretty much everything else is 'in the cloud' already for me. Notion, IA Writer, Slack, 1password, Spotify. All available either via the browser or play store. So far, so got a working machine.

{{> picture alt="A photo of my new chromebook on my table" highRes="/media/chromebook.jpg" url="/media/chromebook.jpg" caption="The Pixelbook!" }}

### Problems

The only problem _I personally_ ecountered was file sharing. Which may sound a little silly in 2018, but hear me out. I'm not a big fan of Drive,  the UX isn't amazing. It's good for docs with other people, but not for my files. However I did discover [Backup & Sync](https://www.google.com/drive/download/backup-and-sync/) which seemed pretty cool. Anything that wasn't in anything else and I needed to share between computers, could just be shared.

Problem is, you can't access that on a Chromebook. It's for Windows and Mac only. Yeh mad huh. Something to do with Chromebooks not being geared as working computers and file storage and something something. I'm hoping this will change in the future.

Dropbox is an option here, but I don't have an amazing amount of space and I'm wary of monthly subscriptions as I very much live on the breadline every month. Plus the big deal here is I couldn't get Dropbox working on my Chromebook. I did all the Linux install things. It did this thing one time I tried, where it went to run and just didn't. Now it goes to open and just hangs :rolling_eyes_and_shrug: If anyone can help with this I would be very grateful.

A couple of other things I've noticed were Slack is very different  and possibly hard to use. I assume because I'm running the android version and it's not geared towards desktop. I can't easily reply to threads and I can't share snippets :sad_face:

You also can't set files to open by default in an app you've installed on Linux... I hope that makes sense. So I can't _make_ HTML files open in Sublime for instance. It's not a biggy as I usually open files _from_ Sublime, but it could possibly get annoying in the future.

Also if you are an emoji fan then you are going to have a :sad_face: :flustered_face: time of it. There's not even a close to complete set. Plus the only way I've found to bring up emojis is via the keyboard link in the toolbar at the bottom. Which only works well if you touch the screen. It's a bit of a broken UX process. I hope this is improved in the future. Even a keyboard shortcut would help.

### Hardware

As I write this the battery is decreasing quite rapidly. Although I suppose I have had it off mains all day, so in reality that's pretty good. I would like it to last until I go to bed in a couple of hours tho... will report back. (Back report: I'm going to get the charger - I've got a lot to do tonight).

It's nice and fast for what I use it for, although I haven't done anything particularly heavy yet. I'll whip up twenty thousand animated svgs in a minute yar.

It's as small and lightweight as my macbook AND THE KEYBOARD IS A DELIGHT. It flips to a tablet, but I never find myself doing that. Maybe over time.

Now I have two, yes two, usb-c ports :winky: I had already dealt with this and have adaptors, so it's kinda nice this is the same as the mac tbh.

### Conclude the things!

Overall it's been a good exercise in making sure all my important things are accessible from everywhere. I was almost there but not quite. Apart from designing, where files are big and software locked down (yes - there are good alternatives, but I _still_ get the odd bit of print work and Illustrator is just my fav).

Would I pay full price for it? I'm not sure I would pay full price for anything on the market right now. Point me in the direction of a system that will run my graphics software _and_ makes a good dev machine (with minimal setup) _and_ lasts more than 18 months, point me in the direction of a worthy investment and I will pay the money.

But actually this is a pretty good option :)

### So what about the mac?

Well I took it into the Apple store. Massive props to [Sam](https://twitter.com/sammachin?lang=en) who made me aware they were _allowing_ us the possibility of fixing the keyboards should they think there _may_ be a problem.

This time I got to talk to a _technician_ :posh_face:. He was really nice, he said he would replace the keyboard, and the battery, and the screen! (The work came in at 200 english pounds less than a new machine... :shrug: go figure). He also wrote a long paragraph about the Ruth Crafted Button™ for his technician friends, he thought it was very clever and thought they would as well.

I got it back today, less than a week, I am glad, now if one computer breaks/gets lost/falls off a cliff, I have the other and they will both work good.


A big thank you to everyone who helped or offered up their spare machines. A working machine is so important and can easily be taken for granted. I'm feeling a lot calmer about my hardware situation right about now!