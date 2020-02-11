---
layout: post
title: "Linux Is Good for You, Part 2: Is Debian too Difficult to Install?"
date: 2018-03-30 14:31:29 +0100
description: Is Debian too hard to install (or at least harder than others)?
category: software
tags: [Linux, OperatingSystem, Debian, ArchLinux]
---
While researching the matter to find the proper answer to Molly’s question (<a href="{{ site.baseurl }}{% post_url 2018-03-29-easy-guide-linux-chromebooks %}">Linux–based operating system to replace Chrome<abbr>OS</abbr></a>), I came across a speech Linus Torvalds gave a while ago, stating that he doesn’t use Debian, “because it’s too difficult to install”.<!--more-->

<figure>
<div class="youtube">
<iframe src="https://www.youtube.com/embed/sd7SMnsEEYM" frameborder="0" allowfullscreen></iframe>
</div>
<figcaption>
<p>Installation of Debian 9 by <a rel="external" title="Youtube channel of Riba Linux" href="https://www.youtube.com/channel/UCuHJawjMUOk4gjywwDg727w">Riba Linux</a>. <a rel="external" href="https://www.youtube.com/watch?v=sd7SMnsEEYM">Watch this video on Youtube</a></p>
</figcaption>
</figure>

I had no doubt that he spoke in jest, but the notion stuck with me. Is Debian really more difficult to install than any other Linux–based operating system?

As a devout “Debianite” for more than a decade, I was confused. Was it my own tendency to a no–nonsense approach to all matters under the sun why I preferred Debian’s installation routine to most of its derivates? Was it my lack of experience with any software outside Debian’s universe?

I had not become a Debian user by choice but rather by circumstance. Tired of the shenanigans of a particular operating system (<abbr>OS</abbr>) from a certain software factory, I paid the software shop I then used to frequent a visit and obtained a copy of the only Linux–based <abbr>OS</abbr> they had on stock.

It happened to be one of Debian’s derivates. Installing it was a easy as pie and it gave me no headaches during daily work; I simply had no need to look any further. Perhaps, I was biased. I had to find out.

So I tested nine randomly picked operating systems and eight desktop environments. Here’s a list in no particular order (terms in parentheses indicate the desktop environments tested with the respective <abbr>OS</abbr>):

<ul>
<li><a rel="external" title="home page of Debian" href="https://www.debian.org/">Debian 9</a> (Gnome 3, <abbr>Xfce</abbr>)</li>
<li><a rel="external" title="home page of Ubuntu" href="https://www.ubuntu.com/">Ubuntu 17.10</a> (Gnome3, <a rel="external" title="home page of Lubuntu" href="https://lubuntu.net/"><abbr>LXDE</abbr></a>, <a rel="external" title="home page of Xubuntu" href="https://xubuntu.org/"><abbr>Xfce</abbr></a>)</li>
<li><a rel="external" title="home page of Linux Mint" href="https://linuxmint.com/">Linux Mint 18</a> (Mate)</li>
<li><a rel="external" title="home page of LMDE" href="https://www.linuxmint.com/download_lmde.php">Linux Mint Debian Edition 2</a> (Cinnamon, Mate)</li>
<li><a rel="external" title="home page of Fedora" href="https://getfedora.org/">Fedora 27 Workstation</a> (Plasma 5)</li>
<li><a rel="external" title="home page of PureOS" href="https://www.pureos.net/">Pure<abbr>OS</abbr></a> 8 (Gnome 3)</li>
<li><a rel="external" title="home page of ROSA" href="http://www.rosalab.com/">ROSA Desktop Fresh <abbr>R10</abbr></a> (<abbr>LXQt</abbr>, Plasma 5)</li>
<li><a rel="external" title="home page of Manjaro" href="https://manjaro.org/">Manjaro 17.1.6</a> (Gnome 3, Plasma 5, <abbr>Xfce</abbr>)</li>
<li><a rel="external" title="home page of Solus" href="https://solus-project.com/">Solus 3</a> (Budgie, Mate)</li>
<li>Gallium<abbr>OS</abbr> 2.1 and Windows 10</li>
</ul>

Windows 10 is listed as a reference system here to give the precious reader some perspective.

(No, I really don’t want to bash Microsoft. If you have — or prefer — to use it, by all means, stick to and be happy with it. No one is to judge you for your choice.)

Gallium I did already discuss in part 1, the <a href="{{ site.baseurl }}{% post_url 2018-03-29-easy-guide-linux-chromebooks %}">article on
Chromebooks</a>. It too shall serve as reference system, representing the other end of the scale (in a way).

Now, let’s start with the things they all have in common (“all” referring to Linux–based sytems only):

<h3>“Live” Sessions</h3>

All may be downloaded as “Live Edition”, which is lovely as it not only lets you test the software prior to installation without disturbing the order on your hard drive, but also may offer early hints on possible compatibility issues with your machine.

Installing the distro from within the Live session is quite comfortable as they usually provide an “install” icon on the desktop which triggers the installation routine.

<h3>Installation in Single–Boot Mode</h3>

All could be installed in single–boot mode without having to fool around with the <abbr title="Basic Input/Output System/Unified Exensible Firmware Interface">BIOS/UEFI</abbr>. If you happen to run into trouble, though, you may want to check the BIOS entry for the “Secure Boot” option and disable it. I discussed this issue in detail in the article about <a href="{{ site.baseurl }}{% post_url 2017-11-27-dual-boot-linux-windows %}">dual–booting Ubuntu and Windows 10</a>.

<h3>Ease of Installation</h3>

What’s considered “easy as pie” or “almost too much to suffer” is a matter of personal taste and attitude rather than one of actual difficulty or technical peculiarities. I did <em>see</em> some minor (and not–so–minor, perhaps) differences with all of them, but I did not <em>experience</em> them — in other words, none bothered me much.

Debian and Pure<abbr>OS</abbr> — which is the one closest to its parent in this respect — take a more conservative approach to “graphical installation” than most of the others, but they compensate this lack of “optical appeal” with good sense. During the installation (rather than after the first login into the new system) you are informed of possible hardware issues and offered to provide additional software to mend these.

<h3>Comfort and Speed of Installation</h3>

When it comes to both comfort and speed, Manjaro (an Arch Linux derivate) is second to none of the tested mainstream distros. Of the candidates above, only Manjaro and ROSA (although written in capitals, it doesn’t seem to be an acronym) provide the user with a menu to select proper language, localisation and keyboard settings <em>before</em> launching the Live session. This makes testing considerably more convenient.

Manjaro also offers to select whether you want free or non–free drivers considered. Debian, on the other hand, offers free and (alternative) non–free downloads of each spin on their website. With Pure<abbr>OS</abbr>, being a 100% Software Libre distro, it is obvious that only free drivers are employed by default. <abbr>ROSA</abbr> informed me that free drivers are employed. The rest did not bother to mention hardware drivers at all.

Don’t expect me to offer accurate figures, as the speed of installation depends vastly on the speed of your machine. Therefore, I introduced the two reference systems.

If Windows 10 may be installed in 20 to 22 minutes (measured from the moment I hit “install” to the moment I was able to log in for the first time), Gallium<abbr>OS</abbr> may be up and running in seven to eight minutes (but Gallium installs not nearly as much software as any of the other candidates).

Manjaro managed a ready–to–go system in nine to ten minutes. ROSA completed the installation routine after 13 to 15 minutes. The rest of the lot took 14 to 16 minutes to arrive at the login screen.

<h3>Installation in Dual–Boot Mode</h3>

Most installations in dual–boot mode were not much more difficult or tiresome than in single–boot mode. All offered “guided” or “automatic” installation, usually taking up the largest free partition available. Most of them took charge of the boot management without ado and presented me with a menu to select systems from after the reboot.

Considering all things said thus far, the few exceptions were quite interesting (to put it mildly).

Solus 3 refused to be installed on a system with an <abbr>EFI</abbr>/boot partition of less than 512 <abbr>MB</abbr>, which is troublesome as Windows affords this partition only around 100 <abbr>MB</abbr>. Resizing the boot partition at this point may put the Windows installation at risk of failing. The only “safe” approach were to create another boot partition for Solus, but this would mean a waste of hard disk space.

It may be possible to find a workaround to solve this conflict and have both systems live peacefully on the same hard drive, but honestly, I didn’t bother to find out. There were just too many options left to spend time on a bearable solution for this issue.

Pure<abbr>OS</abbr> installed just fine, but seized the boot partition, ignoring Windows 10 altogether. Updating the boot manager might solve this issue, but again, too many options left to bother.

This behaviour was insofar surprising as the installation routine is practically identical to Debian’s (which — like any of its “children” — has no problems sharing the hard drive with Windows 10 and taking good care of the boot management).

Whether this is actually a “feature” (in an attempt to drive out proprietary systems) or a bug, I cannot say. If it’s a bug, chances are it will be eliminated anytime soon. If, on the other hand, the developers sideline Windows on purpose, I dare predict Pure<abbr>OS</abbr> is not looking at a bright future outside a rather small circle of die–hard enthusiasts.

The point of Software Libre is to offer the user a choice as to which software to use — this should also include the user’s choice to install proprietary software whenever considered necessary or desirable.

Part 3: <a href="{{ site.baseurl }}{% post_url 2018-03-31-easy-guide-linux-desktop-environment %}">Which Desktop Environment You Use May Be more Relevant than Your Choice of Operating System</a>
