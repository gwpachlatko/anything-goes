---
layout: post
title: How to Remove the Magenta TV App from Your Computer (If that Is What You Really Want)
date: 2021-07-15  14:31:29 +0100
description: "A short tutorial to get rid of the app and a long–winded explanation you definitely should read."
category: software
tags: [Magenta, Apps, Linux, Tutorial]
---

There is quite a number of people who seem to be … well, less than happy with the “Magenta <abbr>TV</abbr> App”. All their requests as to how to get rid of it again seem to be met with the same official statement: “You cannot remove it manually.”

Perhaps it’s just me, but such a bold statement literally begs to be challenged. And, as it turns out, the solution to this issue is about as simple as the app itself.

<!--more-->

If the precious reader happens to be in a bit of a hurry and one to light–heartedly cast sound advice to the winds (which the precious reader should never do), <a href="#howto">let’s skip the yada and get done with it already</a>, but you definitely should at least read the following warning first.

<figure>
<blockquote>
Bloody read the entire article, you have already wasted more time trying to find information on this issue than it takes to read my words!
</blockquote>
</figure>

I’ll be quick, anyway. Promised.

<h3>Windows, Mac, Linux, Desktop, Laptop, Smartphone, Tablet, or What?</h3>

Before we get into the part the more adventurous users have just skipped, here’s what the situation looks like from where I sit. I am using a desktop computer. My operating system is Linux–based. In other words, I’m using a set–up that is commonly considered exotic and thus not supported by mainstream manufacturers (or so the story goes).

Funny enough, I hardly ever run into issues a great many people using any of the mainstream software ecosystems seem to experience. More often than not, I have a harder time reproducing issues I read about than actually solving them. But that’s a different story altogether.

If I do face (serious) trouble, I hardly ever get (useful) answers from manufacturers. Consequently, I have long since given up taking official statements at face value. Manufacturers tend to stick with the mainstream, because they try to avoid receiving random requests concerning exotic issues, only to be publicly told off, if their proposed approach happens to fail (and, to be honest, I cannot blame them).

Yet, what is “you cannot remove it manually” supposed to mean? What else would be the last resort, if all fails? I mean, short of erasing the hard drive, reinstalling the operating system, and setting up the entire system again. No, that cannot be the only “solution” to issues as mundane as this one.

<h3>Apply Common Sense</h3>

However, I cannot promise that my approach will work for everyone and every possible system there is. As I said, I am using a desktop computer and a Linux–based operating system — and that’s the environment I used to reproduce (and solve) this particular issue (for myself). My advice for you, precious reader, is to take away what’s reasonably possible and otherwise apply common sense.

<h3>Why Do You want to Remove the App?</h3>

Now, don’t get me wrong, I’m not prying. It’s entirely up to you what you do with your computer — and how you do it. Yet if your reasons include such generic statements as “it doesn’t work”, or “I cannot stream with it”, or something along those lines, I’m afraid to tell you that I’m inclined to agree with above mentioned mainstream manufacturers. 

If you happen to have privacy concerns — because “one can never be quite sure what such applications do” — I’m rather confident to be able to put you at ease (at least for this once).

Yet before taking things to extremes, it’s always smart to try and figure out what one is actually dealing with.

<h3>What Is this App and What Is It Doing?</h3>

The Magenta <abbr>TV</abbr> App is a tool that’s offered to customers of Magenta <abbr>TV</abbr>, a streaming service, run by Magenta, a mobile carrier (formerly known as T–Mobile). They may go by a different name in individual countries of operation, but you most likely will be able to identify them by their logo (yeah, it’s usually hot pink).

Now, the app itself is basically a so–called desktop application. A file that contains a few lines of code that establish which icon to use to represent the app on your screen, where to find the browser in use, and to associate the launcher with your account. Apart from this, it contains nothing that should give you headaches.

What it does is quickly told: nothing much, really. It opens a window (a browser window, basically) that looks fancy  and that’s that. There are no extra features (compared to streaming without it), and given its size (about 300 bytes) and the lack of relevant code, it’s safe to assume that there is no background activity, either. 

What purpose could any background activity serve, anyway? Spying on you? Rather not. You have to have a user account and log in to their server to use their service. At that point, it is a bit late to have privacy concerns. They already know who you are and which shows you prefer to watch. The app is not likely to make any difference in this respect. If it were to gather information, using it would not be optional.

At any rate, there are no software dependencies, it is literally “standalone”. Neither your operating system nor any of the other programs and applications sharing space on your hard drive are bothered by its presence or absence. So you are free to do whatever you see fit. 

If you came here by accident, desperately trying to find a solution to remove a different <abbr>TV</abbr> streaming app, you may be lucky. It’s quite possible that your issue may be tackled the same (or at least a similar) way.

So what you can do to make streaming possible is enable “Widevine”, when prompted to do so (usually when you launch the service for the first time) — if you missed that opportunity, you may do so in the browser settings (it’s an extension). That should mend all your performance issues (that appear to be browser–related). I trust you will be able to find out for yourself what “Widevine” is.

All said so far applies to streaming movies from Netflix and a great many other services, too.

<h3>Why even Use this App?</h3>

I don’t know, to be honest. If you don’t have more than one streaming service, you could just as well set your browser to launch with your streaming account’s interface. Unless you delete the cookies related to your account, your favourite show is only one click away — whether or not you use that app.

<p id="howto">Now that you are informed enough to make a sound decision go about it at your own discretion.</p>

<h3>How to Remove It?</h3>

Locate the directory (folder) in the file system of your device where all applications (native and/or third-party) are stored. 

It is quite possible that there are several such directories (that depends on your software configuration). In that case, check the one that contains files related to the browser you chose to install the app. There should be a file following this name pattern: <code>nameofbrowser.stringofseeminglyrandomletters-Default.filetype</code>, something like, <code>chrome.noggbhnfgkiiclmcnnnplkapofincllj-Default.desktop</code>. Delete this file. (That “string of seemingly random letters” is your account <abbr>ID</abbr>, by the way.)

If you are on a mobile device and there is an option to uninstall this app, try it. If not, do whatever you did with other apps you wanted to get rid of in the past, and you should be fine.

If you have also deleted your browser cookies, you should be presented with the opportunity to install the app again, as soon as you try to log in to your account. If that’s not what you want, tell it to stop asking.

<h3>Conclusion</h3>

(Note that this is one man’s opinion.) There is nothing wrong with this application. If you want to use it, you are probably best off in a combo with Google’s Chrome. 

Just be aware that third–party applications have a tendency to break, when browsers experience (major) upgrades. So there is always a chance, it turns up dead, because a new browser version is not compatible with the app.

That’s a common issue in computing — and one of the reasons I don’t use this particular app. The other is, I don’t like to clutter the system with software that offers no obvious (considerable) advantage. A fancy outfit for a browser instance is not enough to persuade me — especially so, when it also blocks other (relevant) browser functions (for the duration of a streaming session). Why should I want to launch another browser instance to perform a quick fact check, while watching a show, when I can open another tab instead?

If you have questions concerning this approach or know of a better way to solve this issue in this or any other environment, feel free to let me know. 