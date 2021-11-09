---
title: Netrunner Mobile Random Card
date: 2020-05-18
type: web tool
status: In Progress
excerpt: A web app that displays a random netrunner card.
---
<a href="http://netrunner.pawnstorm.net"><picture><source srcset="/assets/NRRCiS_screenshot.webp" type="image/webp"><img src="/assets/NRRCiS_screenshot.png" style="float: right; padding-left: 1.2rem; padding-bottom: 1.2rem; max-width: 35%;" alt="A srceenshot of the app."></picture></a>

[Netrunner Mobile Random Card](http://netrunner.pawnstorm.net) is a web app (okay, more like a single web page) that I'm working on that is designed to function similarly to the [Netrunner Random Card browser extension](https://chrome.google.com/webstore/detail/random-netrunner-card/ebclfmmncipkjpnpmbefgcdlnobecgeh) for Chrome. It does a couple of things differently, though:
- It is designed for mobile. The Chrome extension doesn't work on my mobile browser of choice (Brave), so this is designed to do that on my phone.
- Currently it picks a card at random from the entire cardpool, but I'm working on setting it up so that it will only show cards currently in standard. This could take a while to implement since I'm learning JavaScript as I go and I'm trying to do it through the API rather than hard coding it, so that I don't have to update it every time a new set or [banlist](https://nisei.net/op/supported-formats) is released.

Without further ado, you can find the project at [netrunner.pawnstorm.net](http://netrunner.pawnstorm.net).

## Notes
- If you're wondering what the heck Netrunner is, you might want to take a look at my [Netrunner New Player Guide]({% link _projects/netrunner-new-player-guide.md %}) which attempts to provide a brief introduction to the game.
- Although this is designed for mobile, since it is loading full-size card images, it has the potential to use quite a bit of data (5+ mb / load), so be warned if you spend most of your time on mobile data rather than wifi. Once I get it to filter down to just cards in standard, I may try to create a lightweight text-only version. However, since one of the reasons I created this was because I'm relatively new and want to get better at recognizing cards while playing on [jinteki.net](https://www.jinteki.net/), this won't be a priority for a while.
- This app consists of only a single page, everything else it gets from the netrunnerDB API, you can download the page and save it on your device to save a bit of data/time.
- Unfortunately, [Brave](https://brave.com/) on mobile (as awesome as it is otherwise) doesn't let me set the default page to load for a new tab, so the hack is to replace the launch shortcut with a link to this (or just to put a link to this somewhere where I can easily use it) which will open the site up in a new tab in Brave.
- Huge thanks to [netrunnerDB](https://netrunnerdb.com/) for creating the database that this is based on. None of this would be possible without them.

## Version History
- **0.3** The image should now link to the displayed card. Now works well enough that I can start working on filtering down to just standard-legal cards.
- **0.2** Getting there. Images should always load now. Also, need to make the image link to the proper record on NRDB.
- **0.1** It (kinda) works! Unfortunately about half of the cards in NRDB have a different image source, so I'll need to figure that out.
