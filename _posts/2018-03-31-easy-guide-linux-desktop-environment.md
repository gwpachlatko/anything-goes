---
layout: post
title: "Linux Is Good for You, Part 3: The Desktop Environment May Be more Important than the Operating System"
date: 2018-03-31 14:31:29 +0100
description: Which desktop environment you use may be more relevant than your choice of operating system.
category: software
tags: [Linux, OperatingSystem, DesktopEnvironments]
---
One of the big advantages of using a Linux–based operating system (<abbr>OS</abbr>) is that one may choose from a wealth of desktop environments (<abbr>DE</abbr>). Selecting the one that is best for your needs may be more important even than your choice of <abbr>OS</abbr>.<!--more-->

It may not be instantly obvious to Windows or Mac<abbr>OS</abbr> users, but unless you work on the command line interface (<abbr title="also known as">a.k.a.</abbr> console, terminal, bash, <abbr>etc.</abbr>) you never actually see your operating system. What you do see is the “Graphical User Interface” (<abbr>GUI</abbr>) or, in Linux parlance, “Desktop Environment” — a different beast altogether.

This bit of information may be of minor relevance to the average user of proprietary systems, as they, apart from a minor tweak here and there, have no choice when it comes to the optical representation of data and processes, but logical shortcomings or even a bug in the <abbr>GUI</abbr> are more likely to cause your machine (and as a consequence, you) difficulties than individual oddities of the <abbr>OS</abbr>.

The proper governance of available hardware and the overall stability of software is the operating system’s responsibility, but the economics of your desktop environment are a “make or break” aspect of your daily experience.

If you read the second part of this series (<a href="{{ site.baseurl }}{% post_url 2018-03-30-easy-guide-linux-installation %}">Installation</a>), you will know that I tested most operating systems with more than one desktop environment. During the installation, the difference (if there actually was any) was too marginal to recognise. After the first login, though, the respective <abbr>GUI</abbr> in use left no room for speculation.

Of all tested candidates, Manjaro was the only one where the inner logic and responsiveness of individual desktop environments made little difference in terms of speed and workflow. In other words, working with the Gnome&nbsp;3 <abbr>GUI</abbr> was almost as convenient as with the <abbr>KDE</abbr> desktop, and <abbr>KDE</abbr> was not perceptibly slower than the <abbr>Xfce</abbr> environment — such, at least, was my experience.

This may to some extent be the result of Arch Linux (the parent distro) sailing with the mainsail properly trimmed at all times, employing the latest available versions of software and the latest kernel reasonably affordable, but for the most part it simply is one fast and efficient operating system. Combine it with a relatively modern, resourceful machine and Bob’s your uncle.

The most interesting detail in this context is that Manjaro was also the only one that worked fine out of the box with only the <a rel="external" title="this term explained on Wikipedia" href="https://en.wikipedia.org/wiki/AMD_Accelerated_Processing_Unit"><abbr>APU</abbr></a> present. In other words, it appeared to be the most flexible of all candidates.

All other distros I tried with Gnome&nbsp;3 had more or less serious issues with <abbr>AMD</abbr>’s graphic processor (I discussed the <a href="{{ site.baseurl }}{% post_url 2017-11-27-dual-boot-linux-windows %}">issues with Wayland</a> in an earlier article already) — some of these could only be addressed by installing a graphic card.

This would actually have nothing to do with the operating system itself, as Wayland is a graphic server, but the support for display–related matters is obviously not of the same quality in individual distros. You would expect Gnome&nbsp;3 to provide an equal user experience under comparable circumstances, regardless of the operating system employed, but this is not the case.

In general, I would say your best bet is to use (links below point to the projects’ respective home page):

<ul>
<li><a rel="external" href="https://www.gnome.org/">Gnome&nbsp;3</a>, when your screen estate is rather limited (and your machine not too low on resources)</li>
<li><a rel="external" href="https://www.kde.org/plasma-desktop"><abbr>KDE</abbr>&nbsp;Plasma&nbsp;5</a>, when you prefer comfort and efficiency (and your hardware can afford it)</li>
<li><a rel="external" href="https://xfce.org/"><abbr>Xfce</abbr></a>, when your machine is a bit weak (or you like to experience more speed)</li>
<li><a rel="external" href="https://mate-desktop.org/">Mate</a> or <a rel="external" href="https://lxde.org/"><abbr>LXDE</abbr></a>/<a rel="external" href="https://lxqt.org/"><abbr>LXQt</abbr></a>, when your hardware is not up to date (or you prefer a traditional desktop metaphor)</li>
<li><a rel="external" href="https://github.com/linuxmint/Cinnamon">Cinnamon</a>, when you prefer a hint more optical appeal than <abbr>Xfce</abbr> or Mate or <abbr>LXDE/LXQt</abbr> provides (and you are prepared to trade in a bit of speed for this luxury)</li>
<li>and <a rel="external" href="https://budgie-desktop.org/home/">Budgie</a>, when none of the others, for one reason or another, manage to convince you</li>
</ul>

Please note that this list of desktop environments is not remotely exhaustive; these are simply the ones I tested. And, make no mistake, all said about them here is merely my personal opinion.

Each of these <abbr>GUIs</abbr> is a fine piece of software in its own right, but I dare to predict the precious reader will not find them equally useful or convenient under all circumstances.

Most distros come with a default desktop environment (and some do even offer a wider range of individually flavoured spins for download), but you may always switch to a different <abbr>GUI</abbr> without having to reinstall the operating system.

This is, by the way, also true for individual applications. You may use software initially developed for the <abbr>KDE</abbr> desktop in a Gnome or <abbr>Xfce</abbr> environment, and vice versa.

Absolute beginners will probably benefit from a more conservative metaphor, as many distros offer quite a range of applications with unfamiliar names and functions. In these cases, proper categorisation could be more helpful than a “sock drawer” with alphabetically ordered items. After all, pinning every application you might find useful to the list of favourites is as good as having none at all — and you cannot possibly create a shortcut for each and everything.

Part 4: <a href="{{ site.baseurl }}{% post_url 2018-04-01-easy-guide-linux-beginner-distros %}">How to Find the Right Linux–based Operating System as an Absolute Beginner?</a>
