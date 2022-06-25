---
layout: post
title: "Windows 11, Part 3: Things I Don’t Get"
date: 2022-04-18  17:31:29 +0100
description: "A short review of Windows 11. Things I don’t get: Microsoft Store, Truncated context menu, Settings, Registry, Control Panel, Power Shell."
category: software
tags: [Windows, Review]
---

<p>Having tested Windows 11 for only four days, I cannot honestly say that I have explored every last bit of it thoroughly (but that had not been the purpose of this trip in the first place) &#8212; and I most certainly did not manage to wrap my head around everything I actually did explore. There may be a number of reasons for that.</p>

<p> That I didn&#8217;t spend more time testing it is certainly one of them; that I&#8217;m not a typical member of Microsoft&#8217;s target group, and therefore lack many years of gradual adjustment, is arguably another. Notwithstanding these limitations, a set of (to me) most obvious questions haunted me for the best part of the past weekend.
<!--more-->

<p>All right, here I sit and admit it: The previous sentence was a poor attempt at placing a clickbait just above the fold &#8212; sorry about that. The questions did not actually haunt me, they just kept popping up at the least expected moments.</p>

<h3>Concept and Execution</h3>
<p>How is it possible that a global player that has been successful enough to make its founder the wealthiest man on this planet (for quite a while), cannot seem to get its act together, while private individuals across the same planet (in the same era) manage to collaborate in order to create, develop, and maintain a vast variety of operating systems and relevant applications in their spare time &#8212; and distribute their produce, more often than not, in a timely fashion and free of charge?</p>

<p>It has been my understanding that Windows is supposed to be a <em>general&#8211;purpose</em> operating system for the <em>average</em> user. Naturally, when it comes to Microsoft&#8217;s marketing strategy I have nothing to offer but poorly informed guesswork, but I can rather confidently state that their definitions of &#8220;general&#8211;purpose&#8221; and &#8220;average&#8221; have little in common with mine.</p>

<p>In recent decades, the most frequently used argument against Linux&#8211;based operating systems (and consequently in favour of Windows) has been that the average user has no (or, at best, little) technical understanding. &#8220;You have to have a strong grasp of the command line&#8221;, some say. &#8220;You will have a hard time getting everything to run properly&#8221;, others pretend to know. Umm, right &#8230;</p>

<p>Here&#8217;s what I have to contribute to this discussion: During the past decade, I have not encountered a single peripheral device &#8212; all of which allegedly compatible with (the latest version of) Windows (at the time of individual release) by default &#8212; that would require more effort to make it work properly under any of the Linux distros I happend to test than it did under Windows.</p>

<p>What about the need to be proficient in the use of the command line, then? Granted, I do make heavy use the bash (at times, for a variety of tasks). Yet the reason for that is (in most cases) not a purely technical requirement; it&#8217;s about speed and efficiency &#8212; the &#8220;average&#8221; user can easily get by without ever launching it. What few routines actually do require the use of the command line under Linux, do also require it under Windows. The actual difference between these &#8220;unequal cousins&#8221; is, that the Linux command line works to the expectation of its &#8220;average&#8221; user.</p>

<p>(I mean, just to provide a random example: The Windows PowerShell asks twice whether or not one wants to &#8220;Terminate [the] batch job&#8221; in response to <code>Ctrl+C</code>, which is supposed to terminate a running routine. What the heck!? Whatever the correct answer to this question in any one case &#8212; be it &#8220;Yes&#8221; or &#8220;No&#8221; &#8212; there is no justification for delaying the process unduly, by asking the same question twice. It is relative safe to assume that respective users know what they want, and why.)</p>

<h3>Microsoft Store</h3>

<p>Try as I may, I cannot see the advantage of having the &#8220;Microsoft Store&#8221; desktop app on the hard drive by default (or at all). I&#8217;m not addressing its quality or usefulness to the average user here (yet), but merely the amount of space it hogs, without serving an immediate purpose.</p>

<p>Every piece of software I happened to find in the Microsoft Store may also be easily obtained from outside this app. Consequently, an online store (accessed via the web browser) would serve the same purpose. One could download whatever software is wanted or needed from a Microsoft server (or strategically placed mirrors) on demand &#8212; a repository, if you will (more about that later).</p>

<p>Downloading software from a remote server &#8212; regardless of the actual source or method &#8212; requires a working internet connection; a desktop app does not make any difference in this respect. Having the Microsoft Store app sitting on the end user&#8217;s hard drive by default (possibly without ever being used) is a waste of mentioned user&#8217;s time and storage space &#8212; which brings us straight to the following two issues.

<h3>Offline Tutorial</h3>

<p>Those 50 <abbr>MB</abbr> were much better invested in a <abbr>PDF</abbr> document that ships with the operating system, providing the average (as well as the more experienced) user with sufficient information as to how everything works. At a rough estimate, that e&#8211;book could run 5000 pages of text &#8212; at any rate, enough to get &#8220;better informed average users&#8221; &#8212; if it ran only one tenth of this page count, there would even be plenty of space left for detailed images.</p>

<h3>Repository</h3>

<p>Wouldn&#8217;t it be considerably more efficient (and arguably also more secure) to provide Microsoft data repositories tailored to respective versions of the operating system (because this is not what Microsoft Store offers)?</p>

<p>This way, every package could be thoroughly tested and reviewed (by Microsoft developers or certified partners), and only then released (to this particular repository rather than the general public).</p>

<p>Beside the obvious advantage that users would only install software that actually is compatible with their version of Windows (as opposed to possibly causing conflicts or dependency issues), they could also decide whether or not they need or want an individual app. After all, there is no point in having apps installed by default, just because they happen to be part of the &#8220;Microsoft Family&#8221;.</p>

<p>(The quality of individual repositories is, by the way, quite often the reason for users preferring certain Linux distros over others. Depending on the individual desktop environment, users have the option to access these repositories via a desktop app &#8212; quite similar to Micorosoft Store, yet considerably better organised &#8212; a traditional software navigator, or the command line.)</p>

<p>That one still has to go hunt down a third&#8211;party tool on the internet, that is, as often as not, more likely to achieve what Microsoft should know better, is a bloody disgrace (if you pardon my French).</p>

<h3>Windows Ink Workspace</h3>

<p>One of the features in Windows 11 I was most excited to test was the allegedly greatly improved Windows Ink Workspace. Well, I already did say that the graphic tablet worked better than it used to in previous versions (thanks to the software its manufacturer provided), so being able to expand its range of usability even further was definitely something to look forward to.</p>

<p>The first time I realised that I could use the pen to scroll up and down a website as though I was using a touch screen, I thought, &#8220;Now you are talking my language, Microsoft&#8221;, and a content smile ran across my face. However, it quickly vanished when I realised that I could not select any text with the pen, because every horizontal movement was also interpreted as a swipe. What the heck!? I had gained one useful feature, only to lose another that is even more useful?</p>

<p>As if that were not bad enough, I could not find this issue even mentioned in the official online documentation &#8212; let alone a workaround. It was pure coincidence that I happened upon a forum thread where exactly this problem was addressed. The proposed &#8220;solution&#8221; was to disable Windows Ink Workspace. This approach did actually work, but was a right bummer.</p>

<p>Interestingly, <a rel="external" href="https://github.com/michalleptuch">Michael &#321;eptuch</a> offers a tool, called &#8220;Ink Workspace&#8221;, in his GitHub repository. It provides everything (except for the swipe feature) Windows Ink Workspace does, and a bit more &#8212; only in a more comfortable fashion.</p> 

<p>Yes, <abbr>Mr</abbr> &#321;eptuch&#8217;s software is also available in the Microsoft Store, but that&#8217;s not exactly the point here. The question is, why does it take two different third&#8211;party applications to accomplish tasks that should be as common as pea soup by now? I mean, we are not talking about some exotic gadget, but a device manufactured by the world leader in this sector and a project Microsoft has worked on for quite a while.</p>

<h3>Office and Its Components</h3>

<p>For the neutral observer, it is difficult to miss that Microsoft is set to develop Outlook to become a centrepiece of sorts of the average user&#8217;s daily workflow, the indispensable sidekick of the likes of Word and Excel and Teams, if you will &#8212; &#8220;ay, there&#8217;s the logical rub&#8221;, to paraphrase old Willie Shakespeare.</p>

<p>Quite recently, I had the opportunity of a sneak preview of the next (projected) version of Outlook &#8212; and I laughed so hard, I nearly fell over. Yes, of course, users <em>could</em> be more efficient, if they had all tools necessary to accomplish their daily tasks in one place &#8212; but why, for the love of Dog, would Outlook, of all available applications, be the centre of action?</p>

<p>Granted, there may be a field of work that more than anythying else relies on the email client &#8212; I cannot seriously be expected to know each and every work environment there may be &#8212; yet I daresay this particular field is not representative of the vast majority of users out there.</p>

<p>Yes, of course, the likes of Thunderbird have, more or less successfully, also tried to establish themselves as one&#8211;stop information management tools, featuring all sorts of components alongside the email client, and this may &#8212; at least in parts &#8212; have informed Microsoft&#8217;s intention to expand Outlook&#8217;s range of use even further.</p>

<p>Yet &#8212; and, precious reader, one really doesn&#8217;t have to be a rocket scientist to realise this &#8212; Microsoft has one significant advantage over any of its contenders: Windows and Microsoft Office (of which Outlook is a part) are family, while the other operating systems and applications are developed independently of one another.</p>

<p>That is, no one can keep Microsoft from seamlessly integrating any or all parts of their Office Suite into the operating system. None of the applications the Office Suite comprises has to be granted permission to immediately interact with the operating system. Not quite clear yet what I mean? Well, here goes:</p>

<p>As soon as the installation of Windows 11 was complete, I clicked the &#8220;date and time&#8221; display (right&#8211;hand end of the taskbar), fully expecting it to open to let me select any one day of the displayed calendar, add an event or task, and set a reminder (which would then show in the notification area, once due), seeing that Microsoft 365 (and therefore also Outlook) was present &#8212; but nothing happened.</p>

<p>I was able to select a day, but this action didn&#8217;t trigger anything. No window to enter an event or task or note, let alone set a reminder, opened. What a disappointment! I was simply given the current weekday and date (information that may also be gathered from one&#8217;s wristwatch or mobile phone, but faster).</p>

<p>So I launched Outlook, and entered an event in the calendar tool to see whether this event would at least be acknowledged in the notification area, by way of marking that day in a different colour or something &#8212; but still nothing. Apparently, these two applications (the calendar in Outlook and the date&#8211;time display of the taskbar) don&#8217;t have access to a mutual database (and consequently no way of exchanging information).</p>

<p>The question begs, why not? Why forgo this decisive advantage? It would be an approach that actually could speed up the user&#8217;s workflow considerably. There would be no more need to launch Outlook every time one wants to add a task or event (or be reminded that a deadline is coming up).</p>

<p>If a user prefers to use, say, Thunderbird and Open Office instead of Microsoft&#8217;s own, fine, but then they&#8217;d get just a date&#8211;time display in the taskbar (just like everyone else, at the time of writing), and lack the advantage of being able to quickly access certain features (and information).</p>

<p>However, to this end, Microsoft would (probably) have to go in a different direction altogether. Rather than developing a user interface to integrate certain components with others, they would have to disintegrate them. That is, develop a first&#8211;rate email client and a calendar (&#8220;Microsoft To Do&#8221; does already exist, and is, in my humble opinion, considerably more useful, anyway) whose relevant content may be accessed, without having to lauch the parent application.</p>

<p>Here&#8217;s how this <em>could</em> work out (at least in my imagination): You turn on your computer, the notification area informs you that it&#8217;s Jane&#8217;s birthday, that you are supposed to attend a meeting at 10.00 and another at 14.30. The reminder of Jane&#8217;s birthday also displays a list of options: &#8220;send her an email&#8221;, &#8220;give her a phone call&#8221;, or &#8220;dismiss the reminder&#8221;. You click the email option, and a small textbox opens for you to enter your best wishes. You hit &#8220;send&#8221;, and click to dismiss the notification. There is no time to check your emails right now, because you are running late for the ten&#8211;o&#8217;clock meeting already.</p>

<p>A number of things went sideways that day and you never got around to even launch Outlook until late in the evening, but at least you haven&#8217;t missed the opportunity to send Jane some digital love on her birthday.</p>

<h3>Settings <abbr>vs.</abbr> Control Panel <abbr>vs.</abbr> Registry</h3>

<p>To put it mildly, having to turn to the &#8220;Control Panel&#8221; or the &#8220;Registry&#8221; to initiate even minor adaptations is a royal pain in the neck. Only very few changes need to be initialised, while the system is booted. So why make such a fuss? (Quite honestly, I cannot even remember when I last had to reboot a computer for any one change to take effect &#8212; most likely when I upgraded from Debian 10 to 11.)</p>

<p>I had to take to the Registry Editor twice and the Control Panel once (and reboot the system each time) inside of the first two days, even though the changes I desired were by no means drastic. Still, even on day four, I haven&#8217;t found a reliable way to set a global viewing mode for items in File Explorer, or keyboard shortcuts to launch certain applications.</p>

<p>For no obvious reason, applications are not responding to a shortcut I have already set several times. Checking these applications&#8217; properties (which happens to be a scavenger hunt of sorts), I find the respective entry to be gone again. Is this merely a bug or an incentive of sorts for the user to keep pinning a launcher of every thinkable application to the Desktop, Taskbar, or Start Menu?</p>

<p>Seriously, if you still employ this abominable tactic &#8220;to gain quick access&#8221;, you have no idea how computers work. Without knowing you in person, precious reader, I can tell you this: The more launchers you have pinned to the Desktop or Taskbar, the less efficient your workflow.</p>

<p>Obviously, every adjustment in &#8220;Settings&#8221; (or the &#8220;Control Panel&#8221;, for that matter) triggers a new (or altered) entry in the &#8220;Registry&#8221;, anyway. So why should the average user even have to bother with the &#8220;Registry Editor&#8221;? And this brings us to the next question &#8230;</p>

<h3>Permissions</h3>

<p>Is it really a great idea to give the &#8220;original&#8221; user (the account &#8220;owner&#8221;) administrator rights by default? On the one hand, the &#8220;average&#8221; user is not considered informed enough to fully customise &#8220;their&#8221; instance of Windows, yet, on the other, they are free to initiate actions the scope of which they have no reasonable way of anticipating? What kind of logic is that?</p>

<p>Interestingly, Windows does know tasks that need administrator rights. Upon initiating these, the user is informed that administrator rights are necessary to go ahead. Yet all it really takes is to acknowledge this statement. So why delay the process in the first place? Do you really think having to hit a button will stop the &#8220;average&#8221; user from doing something foolish?</p>

<h3>One Drive <abbr>a.k.a.</abbr> the Cloud</h3>

<p>Like, what? Making the bold decision to synchronise directories other than those already available by default with the cloud? Oh, wait! That&#8217;s not even possible &#8212; &#8220;superuser&#8221; rights or no.</p>

<p>Why, actually? I could see why third&#8211;party cloud services, such as Dropbox, get their own local directory, if Windows were a particularly security&#8211;conscious system (which it isn&#8217;t, as we all know), but One Drive is a component of Microsoft 365. So why is it not possible to synchronise just about <em>any</em> directory (or file, for that matter) directly with the cloud rather than having to take the detour through another local diretory, which poses the potential risk that some files will not be backed up to the cloud (simply because some users, say, tend to be not quite as careful as one would wish)?</p>

<p>Unfortunately, it doesn&#8217;t even seem to take a sloppy user to &#8220;accidentally&#8221; get rid of documents that were meant to be backed up &#8230;</p>

<p> I am fortunately one of those &#8220;3&#8211;2&#8211;1 backup routine nerds&#8221;, otherwise I might have lost hundreds of files, testing this cloud nightmare &#8212; and this folly would have definitely been discussed in <a href="{{ site.baseurl }}{% post_url 2022-04-18-windows11-review-dislike %}">Part 1, Things I Didn&#8217;t Like (at All)</a>.</p>

<p>(Note for the benefit of the unsuspecting reader: &#8220;3&#8211;2&#8211;1 backup&#8221; refers to the method of having 3 copies of a document, stored on 2 different media and 1 of those copies deposited outside one&#8217;s own environment. Like, one copy on your hard drive, one in a cloud, and one on a <abbr>USB</abbr> drive with a trusted friend or some other safe place. The idea behind this approach is that even if your house should burn to the ground, and provided you survive this disaster, you will still have a working copy of all your relevant documents.)</p>

<p>What&#8217;s the story? Honestly, I cannot even begin to venture a guess, as I have never seen anything similar to that. I copied some directories to &#8220;One Drive &#8211; Personal&#8221; and Windows informed me that the process was complete and all directories had been synchronised with the cloud. Nothing to worry about.</p>

<p>Well, one would have to be born yesterday to believe such promises. Of course, I did check the cloud. Everything looked fine &#8212; at a first, random glance. Yet when I checked the larger directories, I almost lost it. Directories on the first and second level contained other directories and files, but directories on the third level and below contained only empty directories &#8212; not a single file.</p>

<p>Good thing, I still had the originals on the hard drive, right? Right &#8212; except I hadn&#8217;t. Apparently, there is some mechanism at work that synchronises in both directions. Instead of refilling (if they had ever been filled in the first place) the empty directories in the cloud with copies from the hard drive, the directories on the hard drive were also emptied to match those in the cloud.</p>

<p>Even while typing it right now, and having pondered this matter for two days already, I still fail to wrap my head around this absurdity. Why would anyone even implement such a ludicrous mechanism, that&#8217;s utterly contradicting the general concept.</p>

<p>And no, there is no general limitation of clouds that would allow no more than a two&#8211;level file structure, because all cloud systems I have used thus far allow for file structures of any depth &#8212; and not one file went missing to date.</p>

<h3>Security</h3>

<p>Since I dropped the keyword already, let&#8217;s talk about security. Why does Windows 11 still ship with a trial version of a third&#8211;party Security Suite? That seems to indicate that Micorosoft does not put an awful lot of trust in their own &#8220;solution&#8221;. That, in turn, triggers a number of interesting questions. To wit:</p>

<p>How is it that third&#8211;party tools are considered more reliable than anything Microsoft&#8217;s own developers manage to come up with? Or, to put it even more pointedly, does McAfee (the company whose Security Suite ships with Windows 11) know Windows better than Microsoft does? Then, why does Windows 11 even ship with its own Security Suite in addition to McAfee&#8217;s software (which basically renders Windows Security bloatware)?</p>
