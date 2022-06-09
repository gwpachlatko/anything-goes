---
layout: post
title: Dual–Booting Ubuntu and Windows 10
date: 2017-11-27 14:31:29 +0100
description: A no–nonsense tutorial to successfully dual–boot Windows 10 and Ubuntu (and others).
category: software
tags: [Ubuntu, Linux, Windows, OperatingSystem]
---
Quite recently, it came to my attention that a considerable number of people try (and fail) to run Linux–based and Windows operating systems in dual–boot mode on their computers. I tried it myself (just for the heck of it), and here’s how I made such a combination work without major glitches in virtually no time.<!--more-->

<figure>
<p><img alt="Trisquel GNU/Linux (software) logo. A blue triskelion." src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/Logo-Trisquel.svg/500px-Logo-Trisquel.svg.png" /></p>
<figcaption>
<p>Figure: <a rel="external" href="https://trisquel.info/">Trisquel</a> logo without system name on it. Rubén Rodríguez Pérez. Source: Wikipedia. <abbr>GNU</abbr> General Public License</p>
</figcaption>
</figure>

<h3>Some Old Truisms to Consider</h3>
Before we get out to slay some dragons, let me remind you of some old (but still perfectly valid) truisms. I do assume you don’t want to waste time or subject yourself to tedious extra laps and headaches.

Do read the _entire_ article (and be certain to have understood every bit of information it conveys) _before_ you take actions you might regret later.

Do _never_ mess with a working system (you will want to have one handy, should unexpected things occur).

Do _always_ make a backup of documents, applications, and whatever you don’t want to lose in the process of working with intangible media.

If you can help it, keep from mixing apples and oranges. This is to say, if you run an operating system keep to software that was released to be used with this particular system, version, and architecture.

And last but not least, do _always_ install Windows first. The other, Linux–based, operating system will take care of the dual–boot management. (This last one may be taken with a pinch of salt, but there are ways to overcome issues and there are ways to overcome them more comfortably and faster.)

<h3>Preliminary Thoughts (Things to Consider)</h3>
I cannot possibly know your hardware configuration or anticipate what you are about to accomplish with the software you are going to install on your system, as my operating system unfortunately came without a crystal ball <abbr>app</abbr>. Therefore, I shall try to keep this little tutorial rather generic. There is no reason, though, to assume that procedures should be different on a desktop or laptop computer.

At the time of writing, Windows 10 and Ubuntu 17.10 (Codename “Artful Aardvark” or “Artful” for short) are the latest versions out of Microsoft’s and Canonical’s software factories respectively. Thus, these two are going to be referred to here (I’m simply too lazy to mention the version all the time).

The approach described should also work with older versions of Windows (<abbr>i.e.</abbr>, 7 or 8) and it definitely works with Windows 10 and Debian 8 (“Jessie”) or 9 (“Stretch”) instead of Ubuntu (both ran flawlessly alongside Windows in my tests, but Ubuntu was the “distro” most often mentioned in support forums).

[Update, December 2019: Dual–booting Windows 10 and Debian 10 (“Buster”) works as described below. The implementation of Wayland (concerning Gnome 3 desktop, see below) has improved, but is still not perfect. However, that issue has no effect on this tutorial.]

<h3>Preliminary Actions (Things that May or May Not Apply to You, but Are Good to Know in Advance)</h3>
Make sure to have a legal copy of Windows handy — <abbr>OEM</abbr> (Original Equipment Manufacturer, that’s when the software came preinstalled by the manufacturer of the hardware) or standalone (empty hard drive, just the product key or an installation medium with a product key), <abbr>DVD</abbr> (if you have a <abbr>DVD</abbr> drive) or <abbr>USB</abbr> flash drive, it doesn’t matter.

It is also irrelevant whether your hard drive is one of those wheezy, spinning monsters or an <abbr>SSD</abbr> (Solid State Drive) — as long as either is of sufficient size. (The smallest <abbr>SSD</abbr> offered in the shops right now is 120 <abbr>GB</abbr>. That’s plenty of space, as a smart person _always_ stores data other than the operating system and relevant applications outside the system anyway.)

If you have an <abbr>OEM</abbr> version of Windows, but failed to secure the product key, you should be fine as long as you are using the mainboard your computer shipped with, as the product key is stored on it.

Just download a copy of (the same version of) Windows and create a bootable <abbr>USB</abbr> flash drive (there is plenty of information as to how to accomplish this online, so I won’t bother to explain it here) or burn a bootable <abbr>DVD</abbr>. The mainboard will recognise that you are entitled to use Windows.

If you don’t have an <abbr>OEM</abbr> version, you will have to obtain a legal copy (usually on a <abbr>USB</abbr> flash drive) or at least a product key (in this case you can still download a copy of the software from Microsoft’s support site).

<h3>Step 0: Preparing the <abbr>BIOS</abbr> (Basic Input/Output Sytem)</h3>
It should go without saying that your <abbr>BIOS</abbr> has to meet <abbr>UEFI</abbr> (Unified Extensible Firmware Interface) standards, and I assume you know how to access it.

There, enable “Secure Boot” and disable <abbr>CSM</abbr> (Compatibility Support Mode). Set the “Boot Order” to consider the medium containing your clean Windows copy first and the “Boot Mode” to “<abbr>UEFI</abbr>”. If you install from a <abbr>USB</abbr> flash drive, your system will probably set it to be the “primary boot option” by default. This way, Windows should boot without delay or complaint.

<h3>Step 1: Partioning the Hard Drive and Installing Windows</h3>

During the installation process, you will be asked a number of questions as to how you want your operating system configured. Since I have no intention to use Windows as a production environment (and don’t care to possibly be contacted by Microsoft twice a day), I set it to “Offline Mode”. This way, I log in with “name and password” instead of “e–mail and password”. No worries, you will still be able to use it like any other computer and still go online. At any rate, it is not necessary to “create a Microsoft account” for your system to work.

At some point, you will be asked as to how you want the hard drive partitioned. If you let Windows have its way, it will take up the entire space available (regardless of the <abbr>HDD</abbr>’s size).

Delete all partitions Windows recommends, and create two partitions instead. It is up to you how much space you want to afford Windows (the required minimum is said to be 16&nbsp;<abbr>GB</abbr>).

I created two partitions of approximately equal size. (As I said, plenty of space I have no actual use for.) Note: You will have to enter the size in <abbr>MB</abbr> (1 <abbr>GB</abbr> equals 1024 <abbr>MB</abbr>).

If your hard drive happens to provide lots of space, you may want to leave some space at the end of the disk “unused”. It is always possible to access and prepare this space for later use — but much more comfortable without having to reduce already partitioned and properly formatted space first.

Then, select the first partition to be used by Windows (this partition will be divided into four partitions by the software). The rest is mostly waiting for Windows to get its act together. It takes around fifteen minutes to install Windows. Don’t forget to remove the installation medium before Windows reboots, as it won’t warn you to do so.

After the reboot, log in to see whether Windows is working properly, but don’t customise anything. We are not finished yet, and you don’t want to waste time on an environment that might still break.

<h3>Step 2: Revisiting the <abbr>BIOS</abbr></h3>

If Windows works without a flaw, shut it down completely. The reason for a “cold start” is that you have more time to access the <abbr>BIOS</abbr> before Windows comes back again. The “problem” with newer Windows versions is that they don’t reboot completely (which accounts for their alleged booting speed), so do as I say or prepare for several frustrating attempts.

Access the <abbr>BIOS</abbr> and enable <abbr>CSM</abbr> (with “Boot Mode” set to “<abbr>UEFI</abbr> first”) and disable “Secure Boot”.

Once you have changed these settings, the screen resolution during the booting process will be lower. Don’t worry, all’s good.

Plug in the <abbr>USB</abbr> flash drive containing Ubuntu (or feed the optical medium to the <abbr>DVD</abbr> drive) and reset the “boot order” (if you are working with a <abbr>DVD</abbr>) to boot from this drive.

<h3>Step 3: Installing Ubuntu</h3>

Linux–based operating systems tend to come as “Live” systems. That is, you may test them before actually installing them. This may seem to be an unnecessary step, but not all environments are prepared to be run by them without glitches. Most computer configurations are particularly optimised to work with Windows. This is why it makes sense to invest some minutes to check how the new system gets by in your hardware enviroment.

Since the “live” system is run from an external medium, it takes some time to initialise all features and you may also experience some delays when testing it.
This will get a lot better as soon as it boots from a hard drive. (If you failed to turn off the screen reader, just turn off the speakers — unless you are curious how a blind person would experience using a computer.)

If it works without a flaw, install it. There will be a desktop icon for you to comfortably kick off the installation (at least, I have never come across a distro without one).

If you have never before installed a Linux–based operating system, you may be surprised how communicative the software is during the installation process. Unlike Windows (which still only tells you to “please wait a moment”, while displaying some sort of animated circle), Linux–based systems inform you of every step taken and even name the files processed — at the very least you will see a progress bar. Even if that means nothing to you, it makes the installation process less of an ordeal.

You will also be asked some questions in order to configure the system to your taste or needs, but nothing you will fail to wrap your head around.

The partioning procedure should be rather self–explanatory (and you may choose “guided partition” anyway). Nevertheless, I shall not fail to mention that if you have created more than two partitions (during the Windows installation), using the “largest available free space” may not necessarily be want you want. In this case, you should opt for “manual partioning” — and select the partition you set aside for Ubuntu. If your choice is considered “unwise”, Ubuntu will tell you so before “the hurlyburly’s done”.

If you are an absolute beginner, opt for “using one partition” and against a separate “home” partition. Ubuntu will take care of the rest. It will create a swap partition about the size of your working memory. When asked to name a “mount point” for the main partition, choose slash (“/”, without the quotes, of course). This indicates “root”, where all your directories will be stored.

If you are not an absolute beginner, I trust you will find your way around and know how to configure your system without breaking it. I noticed that “Artful”, unlike older versions, does not prompt the user to confirm where to install “<abbr>GRUB</abbr>” (Grand Unified Bootloader), so one thing less for you to consider (and to possibly get you in trouble).

When it’s time to reboot, you will be warned to remove the medium (that’s at least so when you are installing from a <abbr>DVD</abbr>; I have not yet tried to install Ubuntu from a <abbr>USB</abbr> flash drive, but I see no reason why it should be any different).

<h3>Step 4: Reboot</h3>

After you chose to reboot the system, you will get a screen where you can choose between Ubuntu, Advanced Options, the Windows Boot Manager, and System Setup. If you do nothing, Ubuntu will load after a couple of seconds (indicated at the bottom of the screen). That’s the time you have to select which operating system you want to run. (If you select something other than the default configuration, you will have to press “Enter” to continue.)

Leave that alone for now and let the computer boot into Ubuntu, so you will see whether or not it works. If Ubuntu is working, shut down the system. Again, opt for a “hard boot” to give you enough time to access the <abbr>BIOS</abbr>. You will want to set the “boot order” to make your system trying to boot from the hard drive first (not necessary when you installed from a <abbr>USB</abbr> flash drive).

If you don’t, nothing much out of the ordinary will happen, though, as you already have removed all installation media. If your system is reasonably fast, you won’t even experience a considerable delay of the booting process.

As soon as you get to the screen displaying the list of available operating systems again, select the “Windows Boot Manager” and hit “Enter”. Windows should start now. If so, everything is set properly.

This is basically all you need to know to successfully install both Windows and Ubuntu in dual–boot mode. Since you were such a nice and patient reader, I decided to give you a little bonus. Everything said from this point further may be considered “optional reading”, it may or may not apply to your situation, and some may even be boring to the less technically inclined person, but I shall try my best to make the read worth your time.

<h3>Musings of a Die–Hard Pragmatist</h3>

I do understand that some people have no choice as to which operating system to employ. Their daily chores have to be accomplished in a fashion beyond their discretion. It is not for me — or anyone, really — to judge or discuss this in detail.

What I do not understand, though, are people who insist on a certain configuration of hardware or software for no reason other than alleged “stylishness”, or “coolness”, or “superiority”.

If you know what you are doing, it really doesn’t matter whether your computer’s casing bears a divided rectangle, a penguin, or a half–eaten apple for a logo. Likewise, it is relatively irrelevant which operating software you select to run it.

I don’t mean to call anyone out, but insisting on a computer for any of the aspects mentioned above is like buying a car for its colour, brand, or the design of its steering wheel.

As far as I’m concerned, a computer (or any other device, for that matter) is merely a tool. It is — if you are inclined to pardon this metaphor — an employee, minus the benefits. I have no time for complaints about hour of day, day of week, holidays, co–workers (the hardware, in this particular case), and some such.

I want it stable, efficient, and fast from the day of employment to the day of retirement. Not one version of <abbr>MacOS</abbr> nor of <abbr>Windows</abbr> has met any or all of these criteria to this day. Unfortunately, this also goes for Ubuntu 17.10 and Debian 9.

Both “Artful” and “Stretch” came with the Gnome 3 desktop environment, and this seems to be the core issue behind the difficulties a great many people report in forums across the Internet.

After some testing, I noticed that certain issues simply do not occur with the <abbr>MATE</abbr> desktop or the Gnome 3 Flashback environment. I think the problem is, quite similar to Cinnamon (another desktop environment), insufficient (or a total lack of) support of hardware acceleration. The logical result is a “frozen <abbr>GUI</abbr> (Graphical User Interface), while the computer still seems to work”, as the <abbr>CPU</abbr> (the main processor) gets too busy with a workload that should actually be taken care of by the graphic card.

This is particularly obvious as soon as one watches a video (and probably much more so when video games are involved; sorry, no experience there, as I don’t play video games). Videos start with a delay and remain “bouncy”, with a flickering screen when the video player is resized.

Lack of hardware acceleration is quite similar to the bottleneck you create in your office when tasks are delegated to the busiest worker instead of those who actually have the skills to accomplish them more effectively.

There are several reasons for that but one of the core issues is the constant sidelining — or, probably more to the point, deliberate exclusion from the communication channels — of open source developers on behalf of Microsoft.

It may well be that the software factory in Washington State is the wealthiest and most influential actor in the computer universe, the biggest fish in the pond, but in the long run, catering exclusively to them is betting on the wrong horse. “Open source” is not going to retreat or vanish only because Microsoft is not happy with their competition.

If I inspect Windows 10 more closely, it is difficult to miss just how hard they tried to implement certain features that have been known to users of some Linux–based operating systems (and also <abbr>MacOS</abbr> users) for more than a decade. Unfortunately, though, their focus was on the “wrong” features. Instead of making their software more convenient and straightforward, they only made it _appear_ that way.

The questionable approach of implementing “fast” booting (a feature copied from Apple) aside (I explained that briefly already; see above), there is nothing much “under the hood” that came as a surprise.

What did surprise me, though, was the almost obscene hunger for resources — especially so, as the software is obviously meant to also cater to users of portable computers. I cannot possibly know in what respect Number 10 is supposed to be “the best Windows” (Microsoft’s words, not mine; I read it on the screen at some point, while I waited for the software to get its act together), mostly because I am too indifferent to find out, but I do know efficient computing — and this is not it.

Considering that the image (the packed software from which to create a bootable medium) weighs in at 4.7 <abbr>GB</abbr> (compared to somewhere around 600 <abbr>MB</abbr> and 2.6 <abbr>GB</abbr> for Linux–based systems), I would have expected the system to stand on its own two feet after the first reboot (no post–install configuration), with available apps reasonably structured (instead of being listed in alphabetical order), and be ready to work with. Instead, I got “we prepare” here and “please wait” there — not to mention this annoying animated circle, which conveys no information whatsoever.

Of course, proprietary drivers were installed by the system (but not during the installation). Unfortunately, this doesn’t really mean a thing. My graphic tablet and my cheap printer/scanner combo are better supported by any Linux I ever tried than by any Windows version under the sun (despite shipping with software containing “relevant” applications and drivers).

My printer properly communicates with the latest Linux releases without any additional software, and even the scanner is instantly recognised and ready to go.

The graphic tablet does work (that is, I can navigate the cursor) under Windows 10 without additional software, but it seems virtually impossible to get it to each corner of the screen with one smooth move.

Using the Gnome 3 desktop environment, I made another observation concerning the graphic tablet. “Artful” gave me two cursors (one apparently “frozen” centre–screen, and one that may be moved).

It is said that the problem is Wayland, the server now employed by Ubuntu. The quick–and–dirty way to overcome this issue is to fall back to <abbr>Xorg</abbr> upon login (click the cog indicating settings on the login screen and select the legacy server). The “double” cursor will be still there while you log in, but disappear once you enter the system — and everything will work as expected again.

Interestingly, I could not reproduce this issue with a mouse. That’s quite curious, as the tablet otherwise works without a flaw.

<h3>How to Make Sure to Have at Least One Useful and Reliable Operating System on Your Hard Drive</h3>

Since I have no time for such nonsense, I replaced Ubuntu with one of its derivates, Trisquel <abbr>GNU</abbr>/Linux 7 (Codename “Belenos”). It employs a Gnome 3 Flashback desktop environment, which is substantially more responsive than all of the already mentioned systems, while being no “drama queen” at all.

Installing it takes about as long as any of the others, but in terms of performance and instantly available production and configuration software it blows the rest of the lot out of the water.

At least “Belenos” does no more come with the option to install it “alongside Windows” by default, but the partition is not much of a challenge for anyone with comprehensive reading ability and the readiness to follow the advice it offers.

If you want to run it in dual–boot mode with Windows, you best install it from a bootable <abbr>USB</abbr> flash drive. Just follow the steps 0 to 2, and review (and consider) steps 3 and 4 (see above). Then plug in your bootable medium containing Trisquel, and reboot.

Check first whether it actually runs on your computer (“Live”, without installation). If all looks good, double–click the installation icon (it’s a blue triskelion) on your screen. This time, you may leave the flash drive plugged in, as you will want to load the “Live” session again after the reboot.

Once it is fully loaded and running, press <code><abbr>Ctrl</abbr>+<abbr>Alt</abbr>+T</code>. This will open the bash, a terminal window. There, you enter the following three commands (one after the other, in the order indicated). Each of them will be executed after you press “Enter”. The first time, you will be asked for your password (the one you chose during installation; will not appear on the screen). To avoid errors, copy and paste the commands. To paste something into a terminal window, use <code><abbr>Ctrl</abbr>+Shift+V</code>. The three commands are:

<ol>
<li><code>sudo add-apt-repository ppa:yannubuntu/boot-repair</code></li>
<li><code>sudo apt-get update</code></li>
<li><code>sudo apt-get install -y boot-repair && boot-repair</code></li>
</ol>

Let the computer do its job and do as it says. This will install and eventually open a program called “Boot Repair”. If the program fails to start, type “boot-repair” (without the quotes) into the terminal window, and click “Enter”.

A small program window will open and indicate that your systems are scanned. Once the scan is complete, select the pre–selected choice (“Recommended repair”). When you are done, you should be presented with a screen of options during the next booting process. Select “Trisquel” for, well, Trisquel or “Windows Boot Manager” for Windows 10.

<h3>A Few Words on Netiquette</h3>

It seems to me that, of late, “netiquette” has become an old–fashioned, deprecated, or perhaps even already abandoned, virtue. This, I think, is unfortunate. There is no reason to be rude or mindless when communicating with people online. After all, the fewest of “anonymous” bullies and jerks one comes across in the wilderness of the Internet would dare to even consider trash–talking someone else in a face–to–face discussion.

This may be a not–so–new phenomenon, really. I honestly don’t know, as I have long since ceased frequenting support forums. There are just too many people around who “contribute” by randomly telling the world at large that “I have the same issue”. What exactly is this bit of “information” supposed to achieve?

If you are looking for help in a support forum, you are well advised to first look for the right forum to raise your question. If you are an absolute beginner, you may not have realised it yet, but a “pro forum” is _not_ a place where professionals (people who get paid for offering their wisdom) are waiting with hanging tongues to answer your questions (at least not as a rule).

Just read some of the threads already posted. If most of the titles look like gobbledygook to you, it probably is gobbledygook. This is a strong indicator that you are in the wrong place. You may read on in silence (to learn a thing or two), but by all means, do not open a thread with your 101 issue (unless you are a right masochist who enjoys a good “fur–ruffling” or snappy comments on your obvious “n00bility”).

Go ask your provider (of whatever service), the manufacturer of your device, or even the sales person in the shop first. If all fails, ask the neighbour’s kid.

Don’t post technical questions (in any one forum) without also providing pertinent information as to the basic condition of your system or the circumstances of your situation. A smart person will create a signature, including basic system information, so they don’t have to type it anew each time around, save time, and avoid snappy replies (<abbr>e.g.</abbr>, <abbr>ASUS</abbr> H3110–K1TTY, <abbr>AMD</abbr> Unicorn 4x3.0, 64 bit, 8 GB DDR3, Trisquel 7/Win10, …; I made up most of this, so don’t copy and paste it).

Never ever let your (perhaps genuine) question be followed by another posting reading something along the lines of “so you suckers don’t know the answer, either”. You cannot afford the bad karma such behaviour will earn you.

Most forums are moderated and monitored pro bono by a handful of people at most. So, by all means, allow for a reasonable response time and don’t get disrespectful or impatient when you don’t like (or immediately understand) the answer. Answer the questions you are asked in return to the best of your knowledge. Trying to remotely diagnose issues is difficult enough without such shenanigans.

Things don’t look much better, though, on “the other end of the table”. Obviously, some people do get a kick out of trolling unsuspecting individuals, disseminating unchecked, and therefore mostly outdated or even wrong, information, and openly telling people off for being not up to their own high (and often enough questionable) standards. If you don’t know the answer to a question, say so — or, if that’s too much for your ego to suffer, remain silent.

 While researching for this article, I came across a thread in the Trisquel support forum where some “weathered” users literally bullied a poor fellow, who had raised a genuine (and valid) question, for admitting to have installed Windows on his machine.

“This forum does have a tradition to discourage users from employing proprietary software. Therefore, we refuse to help you.” Seriously? This is your attitude when people make an effort to switch from proprietary to open source software? Then here’s my advice: Install your forum where it cannot be accessed from the Internet, so you can resume your circle jerk without disturbance.

Discouraging others from using software other than your own — be it proprietary, open source, or even <abbr>GNU</abbr> (that is, Software Libre) — is exactly the methodology employed by manufacturers of proprietary software to sideline their competition.

Way to go! You have successfully positioned yourselves in the corner of those you pretend to fight to the last — without even realising it. Cheap little soldiers who volunteer to burn down their own camp to keep the fire from spreading. Ma says she’s proud of you.

Seriously, if you rally for Software Libre only to feed your inner rebel in a rather comfortable way, you are no better than any “digital nationalist” who swears by his own software, thinking he’s superior to the rest of the lot, simply because the rest of the lot is supposedly inferior to him.

Since Trisquel releases are usually based on the penultimate Long Term Support (<abbr>LTS</abbr>) release of Ubuntu, you have a good chance to find useful answers to your Trisquel–related questions in the Ubuntu support forum.

As much as I love to use Trisquel — for both the fact that its developers go to great pain to replace all proprietary features with free software (free as in “free speech”, as they say, not necessarily as in “free beer”) and the way it works — I avoid their support forum like the plague. If you are set to gain followers or only make friends, you will have to be prepared to be a friend first.

Being a decent, reasonable person and showing others some respect (face–to–face or in an “anonymized environment”) will not cost you an arm and a leg. An “open web” (or “open society”, for that matter) will not sprout from planting restrictions and cherishing an exclusionist paradigm.

<abbr>PS</abbr>: Upon booting and terminating Trisquel sessions, you will see lines of messages running across your screen. Don’t worry, that’s normal. Every operating system is going through these routines — but most are trying to hide this fact from you at all cost. If all goes well, you may ignore these lines, but if something goes wrong, you will have a starter to look for solutions.
