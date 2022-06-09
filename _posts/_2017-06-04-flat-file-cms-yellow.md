---
layout: post
title: Rainy Afternoon or Why I Switched to Yellow
date: 2017-06-04 14:31:29 +0100
description: If you want to run a blog with a flat-file CMS, you definitely should consider Yellow.
category: software
tags: [Yellow, CMS, FlatFile, WordPress, Grav, TYPEMILL]
---

I have been toying with the idea of switching to another Content Management System (<abbr>CMS</abbr>) for quite a while. It was my general reluctance to change working systems that kept me from making the move earlier. Truth be told, I’m not much of a status–driven person, I don’t care for the brand of my cars and even less for what people have to say about the software I employ to manage my writing. Whatever works with a minimum of fuss is fine and dandy.<!--more-->

<h3>The Challenge</h3>

But a few days ago, two unexpected events — bad weather and a server update — made me sit down and consider my options. The first forced me to stop outdoor work and seek shelter in my study, and the latter caused considerable chaos among dutifully converted special characters in the database, resisting any reasonable approach. If there ever was a perfect moment to try and explore new technical frontiers, it was there and then.

<h3>The Strategy</h3>

It was clear that switching to a new <abbr>CMS</abbr> meant to invest time in order to get to grips with software I was not familiar with. It also meant spending some more time customising the new system. And, as likely as not, I would have to migrate the content manually. That’s the most important factor to consider when using a less popular but highly customised system.

To keep this project from expanding beyond bearable limits, I tried to stay in my comfort zone rather than go overboard with the possibilities the market has to offer. So flat–file systems (these use plain text files rather than databases to store data) that made use of server–side scripting languages other than <abbr title="PHP: Hypertext Preprocessor; that’s a recursive acronym">PHP</abbr> didn’t make the shortlist. And engines that have to be fed pure <a rel="external" title="Visit John Gruber to check out Markdown" href="https://daringfireball.net/projects/markdown/">Markdown</a> ranked very low.

Don’t get me wrong, Markdown is fantastic, if you don’t know the first thing about <abbr title="HyperText Markup Language">HTML</abbr>, but I prefer to stick to “Markup” when it comes to web documents.

<h3>Making No Prisoners</h3>

I wouldn’t recommend this step for everyone to quickly find a winner — if you are not comfortably at home in the web design/development corner, try one system at a time — but after installing several systems shoulder to shoulder, and assaulting them with gusto, I had soon separated the chaff from the wheat.

Twenty minutes later, I was down to two (out of the initial fourteen) candidates that I was prepared to consider for further examination. That may sound like an impossible task, but it really is not.

Some failed to convince me already seconds into the setup process, others would ask for more than the average server features to be present or refuse to launch at all, and some came with more bells and whistles than I could possibly care for. A <abbr>CMS</abbr> is only software. There is no need to be polite. None of the rejected candidates burst into tears.

It may appear counter–intuitive to some, but I prefer <abbr>CMSs</abbr> without paint and tinsel. No “admin panel”? No problem. A backend that’s there to distract the user’s eye from grave shortcomings (like an overall instability, too much maintenance demands, an inconsistent internal structure, <abbr>etc.</abbr>) and pretend “ease of use”? Big problem. No plugins at all? Hmm, there are ways to get what one wants or needs. Plugins that fail to properly work along with others or the core system? Not in a million years. That’s inviting throbbing headaches some time soon.

<strong>Rule of thumb: Do not fall for pretty words. If you happen to read “ease of use” or “easy to customise” in any one software’s description, prepare to run — especially, when either or both are mentioned more than once. The more often such is stressed, the less it is true.</strong>

In general, I prefer open, reasonably flexible systems. You better not give me that “optimised for particular use” crap, for if you have me follow you into that alley, you’ll have to offer one tremendous piece of code to get away with it.

<a rel="external" title="Visit Sebastian Schürmanns to check out TYPEMILL" href="http://typemill.net/">TYPEMILL</a> is such a candidate (in its present stage particularly built for easy–to–maintain online documentation: books, tutorials, <abbr>etc.</abbr>), and I cannot wait to use it for a project or five anytime soon — yet it is a rare exception to the rule.

<h3>And the Winner Is …</h3>

The <abbr>CMS</abbr> I ultimately chose to be the new home for my blog, is <a rel="external" title="Visit Datenstrom to check out Yellow" href="https://datenstrom.se/yellow/">Yellow</a>. It’s unlikely to be the average <a rel="external" title="Visit WordPress to check out their CMS" href="https://wordpress.org/">WordPress</a> (or even <a rel="external" title="Visit Grav to check out their flat-file CMS" href="https://getgrav.org/">Grav</a>) user’s first choice, but it really keeps the fuss to a minimum, and the content reasonably organised.

All data is stored in plain text files, which allows for working offline without having to maintain two databases (simple update via <abbr title="File Transfer Protocol">FTP</abbr>; but you may also edit the visible content in your browser, if you so prefer); it allows for Markdown as well as <abbr>HTML</abbr> to format your documents; works with vanilla <abbr title="Cascading Style Sheets">CSS</abbr>; and features useful plugins (some stable, some experimental) that integrate unobtrusively (I tried two experimental plugins that failed to work, without wreaking havoc — they were simply not available).

What customisation took place was minimal. I tweaked the code a little bit, hardly touched the original <abbr>CSS</abbr>, and added some useful plugins. Considering the time investment, I am happy enough with the result. The migration of previously published articles will occur as time permits.
