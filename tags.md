---
layout: page
title: Tags
permalink: /tags/
---

{% comment %}
=======================
extract all tags from posts and sort them
=======================
{% endcomment %}
{% assign rawtags = "" %}
{% for post in site.posts %}
	{% assign ttags = post.tags | join:'|' | append:'|' %}
	{% assign rawtags = rawtags | append:ttags %}
{% endfor %}
{% assign rawtags = rawtags | split:'|' | sort %}

{% comment %}
=======================
remove dulpicated and invalid tags
=======================
{% endcomment %}
{% assign tags = "" %}
{% for tag in rawtags %}
	{% if tag != "" %}
		{% if tags == "" %}
			{% assign tags = tag | split:'|' %}
		{% endif %}
		{% unless tags contains tag %}
			{% assign tags = tags | join:'|' | append:'|' | append:tag | split:'|' %}
		{% endunless %}
	{% endif %}
{% endfor %}

{% comment %}
=======================
list all the tags used in site
=======================
{% endcomment %}

<h3>Tags Used in Articles</h3>

<div class="tag-list">

{% for tag in tags %}
	<a class="tag" href="#{{ tag | slugify }}"> {{ tag }} </a>
{% endfor %}

</div><!-- /tag-list -->

{% comment %}
=======================
list all posts sharing a certain tag
=======================
{% endcomment %}
<h3>Articles by Tag</h3>
{% for tag in tags %}
<dl>
	<dt id="{{ tag | slugify }}">{{ tag }}</dt>

	 {% for post in site.posts %}
		 {% if post.tags contains tag %}
		 <dd>
		 <a href="{{ post.url }}">
		 {{ post.title }}</a> <small>on {{ post.date | date_to_string }}</small>
		</dd>
		 {% endif %}
	 {% endfor %}
	</dl>
{% endfor %}
