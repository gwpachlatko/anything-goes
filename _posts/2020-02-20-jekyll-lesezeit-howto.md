---
layout: post
title: “Jekyll Lesezeit” Ultimately Explained!
date: 2020-02-21 14:31:29 +0100
description: A detailed explanation how Jekyll Lesezeit came to pass and how to deployit for full effect.
category: software
tags: [Jekyll, Lesezeit, Tutorial]
---
During the past hour I realised that this project might get quite a bit confusing for the random reader, but also for the weathered blogger and developer. So precious reader, if you are interested in this collection of scripts (and perhaps need some hints to use it to effect), here’s the unabridged version of how it all came to pass and how to put it to good use.<!--more-->

### So, What’s the Story?

It started as a rather relaxed project. All I really wanted for my German blog, <a href="https://gwpachlatko.github.io/emwd">1 Minute Webdesign</a>, was to display a word count and the estimated reading time for articles  — but then the damn thing sort of exploded. Since I had never seen these features in German–speaking blogs, I decided to write a nice little script to accomplish as much. That task was only a matter of minutes, so I went a step further and expanded it to display information in various languages. (It was merely an afterthought, really.)

I had already been lucky enough to find <a title="See the repository on GitHub" href="https://github.com/oncleben31/jekyll-date-basic-i18n">a lovely solution to tweak dates</a> by a fellow who calls himself <a title="Visit oncleben31 on GitHub" href="https://github.com/oncleben31/">oncleben31</a>.

[As I checked Uncle Ben’s GitHub link for validity, I realised that I had found Ben’s script through a different channel, and had actually followed the path to one of his other repositories. Thus, I was until right now not aware that he’s been providing a variety of language files for quite some time in his repository already. This renders most of what I have to say about customised dates redundant. Nevertheless, for reasons I will explain below, I think it was still worth the effort.

Also, please know that neither <em>Jekyll Lesezeit</em> as a repository nor any file it contains is competing with any other repository here on GitHub or elsewhere. If anything, it (they) is (are) meant to complement any existing project, if considered necessary.]

Testing my script, I figured that it made little sense for the reader to have the word count and reading time in one language, and the date of the publication in another. And what about the “next” and “previous” links? So I wrote some more code … and yet more.

Now, here we are: One can have a, say, German–speaking blog, and still write individual posts in other languages, with “read more” link, publication date, word count, reading time, and the “<abbr>prev/next</abbr>” navigation in the respective post language. And it’s rather easy to implement the scripts — individually or combined.

At the time of writing these lines, there are six languages available: English (default), German, French, Italian, Spanish, and Portuguese.

### Why the Funny Name?

I called the initial script to include in my own blog <code>lesezeit.html</code> to be able to easily identify the file in the directory tree. <em>Lesezeit</em> is German for “reading time”, and I think it makes for a nice name for the entire repository, as it is for once a German word that’s relatively easy to spell and pronounce, even for most foreign speakers. And the “Jekyll” part of the name refers to the system it was written for (but you probably guessed as much already).

### So How Does It all Work?

The repository <em>Jekyll Lesezeit</em> contains — at the time of writing — nine files (not counting the nearly ubiquitous “README”):

<ul>
  <li><code>lesezeit.html</code> (displays word count and reading time in the post or site language)</li>
  <li><code>readmore.html</code> (displays “read more” on the home page in the post or site language)</li>
  <li><code>prevnext.html</code> (displays “previous” and “next” in the post language)</li>
  <li><code>en.yml</code> (English weekdays and months)</li>
  <li><code>de.yml</code> (German weekdays and months)</li>
  <li><code>fr.yml</code> (French weekdays and months)</li>
  <li><code>it.yml</code> (Italian weekdays and months)</li>
  <li><code>es.yml</code> (Spanish weekdays and months)</li>
  <li><code>pt.yml</code> (Portuguese weekdays and months)</li>
</ul>

#### Display Date of Publication in Various Languages

If you want to display publication dates in a language other than the default English, use the “translated date script” (see links above) and Ben’s your uncle. If your blog is written in any of the other languages mentioned above, you may find the language files I provide quite handy. The reason for providing my own <code>en.yml</code> is that I tweaked Ben’s original a wee bit for the output to comply with <abbr>HTML</abbr> standards as regards abbreviations. Also, the output of the individual files will comply with date conventions of the respective language.

Just pick the language file(s) you need and copy it (them) into the <code>&#47;&#95;data&#47;locales&#47;</code> directory of your blog. Once you call Ben’s script, it (they) will display the dates according to your settings.

In your <code>&#95;config.yml</code> set your blog’s global language: <code>lang: xx</code> (replace xx with the desired language code: “<abbr>fr</abbr>” for French, “<abbr>it</abbr>” for Italian, <abbr title="and so on">etc.</abbr> — without the quotes, of course).

If you wish to have posts in different languages (anything other than the global language, that is), set the desired language in the “frontmatter” of the respective post:

<pre>
---
title: The Post You Want to Write in Another Language
<strong>lang: xx</strong> &lt;!-- again, replace xx with the code of the
desired language --&gt;
date: YYYY-MM-DD HH:MM:SS
description: yada yada
---
</pre>

I changed my own scripts to comply with the standard in Jekyll to keep confusion at a minimum. So whenever you forget to set the custom language (or if the language you set is not part of the opus yet), the output will always fall back to English.

#### “Read More” link and “Previous/Next” Navigation

Both <code>readmore.html</code> and <code>prevnext.html</code> work like any old “include”. Place them in the <code>&#47;&#95;includes&#47;</code> directory of your blog and call <code>readmore.html</code> from your <code>home.html</code> layout and <code>prevnext.html</code> from your <code>post.html</code> layout: <code>&#123;&#37;&#45; include readmore.html &#45;&#37;&#125;</code> and <code>&#123;&#37;&#45; include prevnext.html &#45;&#37;&#125;</code>.

“Read more: ” will appear in the post’s language (as opposed to the global site language), followed by the post title as a link to the article.

Just as the “read more” link, I have seen the “previous and next” navigation in many blogs in different situations already. It always struck me as funny to have content in one language and those links in another.

Depending on your individual settings, the script will display “previous” and “next” in the respective language.

#### Troubleshooting

As expected, it was German that in combination with other languages led to problems. To have some wiggle room when messing with different dates, I omitted dot (after day) and comma (after month) in the date format of posts (<code>format=&#34;&#37;A, &#37;-d &#37;B &#37;Y&#34;</code>), as none of the other languages strictly require them. To me, it was an obvious decision: five times “nay(ish)”, once “aye” means “nay” — but then “Karl–Heinz” came along and demanded his dot after the ordinal.

The easiest workaround to keep the language files as system–agnostic as possible (and not mess with Uncle Ben’s code), and still give Karl–Heinz his beloved dot, was to squeeze a wee bit of additional code into the <code>post.html</code> layout. Like so,

<pre>
&lt;p class=&#34;post-meta&#34;&gt;
  <strong>&#123;&#37; if page.lang == &#34;de&#34; &#37;&#125;
  &#123;&#37;&#45; include translated_date.html date=page.date
  format=&#34;&#37;A, &#37;-d. &#37;B &#37;Y&#34; &#45;&#37;&#125;
  &#123;&#37; else &#37;&#125;</strong>
  &#123;&#37;&#45; include translated_date.html date=page.date
  format=&#34;&#37;A, &#37;-d &#37;B &#37;Y&#34; &#45;&#37;&#125;
  <strong>&#123;&#37; endif &#37;&#125;</strong> — &#123;&#37;&#45; include lesezeit.html &#45;&#37;&#125;
&lt;&#47;p&gt;
</pre>   

This way, the ordinals in German posts appear with and all others without the dot: “Freitag, 21. Februar 2020” (in German) but “Friday, 21 February 2020” (in English), “viernes, 19 de febrero de 2020” (in Spanish), and so on. Not a big deal, especially since you will mess with the layouts, anyway.  

### Why Even Bother?

 I don’t know if the precious reader has ever visited foreign language blogs. It can be quite intimidating for more sensitive readers to not immediately know their way around. One may understand the content of the article all right, because it happens to be in one’s native or in English, but the buttons and links immediately surrounding it may be in a language one is not familiar with. Hovering over them to wait for additional information to pop up is no use either, as this information — so there is any at all — is usually also in the language one is not familiar with. Is it any use to push this button or is it fine to follow that link?

 Clearly, a visitor who navigates to an article from the home page does already know that the site’s global language is different from his or her native, but those following an external link may not. We all should remember that visitors often struggle with supposedly petty challenges designers did either dismiss as irrelevant or not consider at all.

### Notes

#### Markup Standards

I already mentioned markup standards above. I noticed that Jekyll itself does not mark up abbreviated weekdays and months as abbreviations by default: the source code reads <code>21 <abbr>Feb</abbr> 2020</code> instead of <code>21 &lt;abbr&gt;<abbr>Feb</abbr>&lt;&#47;abbr&gt; 2020</code>. I worked around this by writing the abbreviation tags into the individual language files.

#### Cultural Peculiarities

Different cultures tend to have different date conventions. Apparently, it’s less to do with the particular language, but with individual traditions. Some of that may be mended by “hacking the logic of the system” itself (<abbr>e.g.</abbr>, you add or omit a dot in the given date format, or set or omit a comma). That’s fine and won’t “disturb the system’s circles”.
Yet I’m not particularly crazy about more drastic measures, especially if I have to employ a language file, anyway.

Therefore, I wrote the “peculiarities” directly into the individual language files. So, for example, “Friday” will appear in Portuguese as “sexta–feira” and “<abbr>Fri</abbr>” as “sexta” (as I considered “6<sup>a</sup>.” a tad too informal for a blog post). Following the date conventions on this page,  today’s date would read “sexta–feira, 21 de fevereiro de 2020” rather than “sexta–feira, 21 fevereiro, 2020”. (I can only hope that those who already stopped reading did at least read the “Troubleshooting” part.)

#### Copyright

If you are going to use Ben’s scripts, consider yourself advised to acknowledge his copyright notice. As far as <em>Jekyll Lesezeit</em> (<a title="check out Jekyll Lesezeit on GitHub" href="https://github.com/gwpachlatko/jekyll-lesezeit">the scripts in this repository</a>) is concerned, anything goes.

#### Live Demos

<ul>
<li><a title="follow this link to the German Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-german.html">German Live Demo</a></li>
<li><a title="follow this link to the English Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-english.html">English Live Demo</a></li>
<li><a title="follow this link to the French Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-french.html">French Live Demo</a></li>
<li><a title="follow this link to the Italian Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-italian.html">Italian Live Demo</a></li>
<li><a title="follow this link to the Spanish Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-spanish.html">Spanish Live Demo</a></li>
<li><a title="follow this link to the Portuguese Live Demo on my German blog" href="https://gwpachlatko.github.io/emwd/fehlersuche/2020/02/19/testing-lesezeit-portuguese.html">Portuguese Live Demo</a></li>
</ul>

That’s all for now. If there’s anything you need (or just want to know) left, shoot me a mail or drop a note in the comments. If you happen to find typos or grammatical blunders in the live demos, be good enough to let me know. Cheers.
