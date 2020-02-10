---
layout: post
title: "Linux Is Good for You, Part 1: Which Linux–Based Operating System Best to Install on Chromebooks?"
date: 2018-03-29 14:31:29 +0100
description: What Linux-based operating system best to install on Chromebooks when ChromeOS is not an option.
category: software
tags: [Linux, Operating System, Chromebooks]
---
Not so long ago, Molly posed an interesting question, asking which Linux–based operating best to install on a Chromebook to replace Chrome<abbr>OS</abbr>. Finding an answer to this question is not as easy and straightforward a quest as one might expect.<!--more-->

<figure>
<div class="youtube">
<iframe src="https://www.youtube.com/embed/-b900XyKxsg" frameborder="0" allowfullscreen></iframe>
</div>
<figcaption>
<p>5 Lightweight Linux Distros for your Chromebook by <a rel="external" title="Youtube channel of Fascinating Captain" href="https://www.youtube.com/channel/UCtiB4NowvRh14Mer04BWHcg/">Fascinating Captain</a>. <a rel="external" href="https://www.youtube.com/watch?v=-b900XyKxsg">Watch this video on Youtube</a></p>
</figcaption>
</figure>

Initially, I had a simple answer ready: A Chromebook is only a computer. If one distro is able to run the device, there is no sound reason to assume most or all others (of the same architecture) wouldn’t. Admittedly, it was a point–blank shot.

Of course, there is always a chance that one or more operating systems fail to handle any or all components of your device properly, while the rest of the lot do, but a machine that resists more operating systems than it complies with has to be built yet — Chromebooks are not that unique (but it’s a good idea to find out the core architecture of the <abbr>CPU</abbr> your device employs, or you will risk to get lost in “data nirvana”).

There is even a distro that is said to have been built to run Chromebooks exclusively. It’s called <a rel="external" title="Go to home page of GalliumOS" href="https://galliumos.org/">Gallium<abbr>OS</abbr></a>, a <a rel="external" title="Go to home page of Xubuntu" href="https://xubuntu.org/">Xubuntu</a>–based distribution.

Unfortunately, I don’t have access to a Chromebook, so I cannot say whether or not it lives up to the promise. What I can say, though, is that one should not believe everything that happens to be published online.

I read somewhere that Gallium won’t run on computers other than Chromebooks. This is not true. A computer may have to feature one of a rather small range of processors for Gallium to work out of the box, but it does not have to be a Chromebook.

Unlike other Linux–based distros, Gallium<abbr>OS</abbr> is not offered with a range of “flavours” (desktop environments). Instead, downloads are dedicated to individual graphic processors used in Chromebooks or Chromeboxes. I was curious as crap — and lucky enough to remember that my “lab bunny” happens to employ one of the processors listed.

The image one may download is rather small — only 1 <abbr>GB</abbr> — so I did expect a starved–into–submission spin of Xubuntu. Yet it contains a smoothly working operating system that may run any general–purpose <abbr>PC</abbr> (almost) without a flaw.

The sound processor was the only component that did not work on my <abbr>PC</abbr> without ado, but that’s merely a minor issue. Given that Gallium is an <a rel="external" title="Go to home page of Ubuntu" href="https://ubuntu.com/">Ubuntu</a>/<a rel="external" title="Go to home page of Debian" href="https://www.debian.org/">Debian</a> derivate, the odds are in favour of a proper driver being found in the Debian repository.

What distinguishes Gallium from Xubuntu is the choice and number of applications and the kernel configuration. Gallium comes with software requiring even less resources (where available) and has no e–mail client pre–installed (which makes proper sense as the average Chromebook user is likely to use webmail).

Given that the experience is otherwise fast and smooth (slightly faster than Xubuntu, actually), investing a couple of hours (if need be) to track down a working sound driver would be no unreasonable effort.

I have no way of telling just how many computers (other than Chromebooks, that is) out there feature one of these processors, but considering that at least the mainboard I used to test Gallium is still sold regularly (after more than four years), I would assume their number is not quite marginal.

There is a set of scripts (<a rel="external" title="Read description of scripts, usage, options, and compatibility" href="https://chrx.org/"><abbr>chrx</abbr></a>) available for free download to help install a variety of Linux–based operating systems alongside Chrome<abbr>OS</abbr>. While this is rather irrelevant in the given context, knowing about it makes room for some educated guesses.

Since it is possible — by which means ever — to use operating systems not particularly tailored for Chromebooks, the resources provided by these devices have to be sufficient. If they are sufficient, the quality of hardware is not an issue.

Since it is possible to run them in dual–boot mode, it should also be possible to run them in single–boot mode (without Chrome<abbr>OS</abbr> being present, that is).

Since there exists an open source version (Chromium<abbr>OS</abbr>) of the original operating system (and the Gallium<abbr>OS</abbr> project), relevant drivers have to be publicly accessible through one channel or another.

A promising starting point for further investigations is, probably among others, <a rel="external" title="see how to install Debian on a wide range of machines" href="https://wiki.debian.org/InstallingDebianOn">DebianOn</a>, a “Wiki” providing tutorials to install Debian on a variety of devices.

Without a Chromebook, and with only one test configuration, it was not possible to ultimately confirm or falsify any of these conclusions. Yet my curiosity was kindled, and I wanted to at least establish part of my driver–not–resources–issue theory.

Unless I was completely wet, the version of Gallium I had downloaded would work even on a configuration not featuring this particular graphic processor. With access to a machine employing one of the range of “Chromebook processors”, finding proof was not much of task.

I installed Gallium on a hard drive in the lab bunny, downloaded and installed a graphic driver for the production machine, and eventually booted it with the test hard drive housing Gallium plugged in.

Without the graphic driver, the machine had not even completed the boot process correctly (which was to be expected), but with the driver properly installed, it not only booted without a flaw, but also ran smoothly (and really fast). Even the sound issue lab bunny had thrown was gone.

For a moment or two, I seriously considered switching to Gallium for good — if only customising a production environment were not such a hassle. That’s not something one does just for the heck of it (at least not, if one is anything like me).

(At that moment, I had no idea I would do exactly this in favour of one of the other candidates only a day and a half later.)

Part 2: <a href="{{ site.baseurl }}{% post_url 2018-03-30-easy-guide-linux-installation %}">Is Debian too Hard to Install (or at Least Harder than Others)?</a>
