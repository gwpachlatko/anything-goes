---
layout: page
title: Categories
permalink: /categories/
---
{% assign rawcategories = "" %}
{% for post in site.posts %}
	{% assign tcategories = post.categories | join:'|' | append:'|' %}
	{% assign rawcategories = rawcategories | append:tcategories %}
{% endfor %}
{% assign rawcategories = rawcategories | split:'|' | sort %}

{% comment %}
=======================
The following part removes dulpicated categories and invalid categories like blank category.
=======================
{% endcomment %}
{% assign categories = "" %}
{% for category in rawcategories %}
	{% if category != "" %}
		{% if categories == "" %}
			{% assign categories = category | split:'|' %}
		{% endif %}
		{% unless categories contains category %}
			{% assign categories = categories | join:'|' | append:'|' | append:category | split:'|' %}
		{% endunless %}
	{% endif %}
{% endfor %}


{% for category in categories %}
<dl>
	<dt id="{{ category | slugify }}">{{ category | capitalize }}</dt>
	 {% for post in site.posts %}
		 {% if post.categories contains category %}
		 <dd>
		 <a title="Read article: {{ post.title }}" href="{{site.baseurl}}{{ post.url }}">
		 {{ post.title }}</a> <small>on {{ post.date | date_to_string }}</small>
	   </dd>
		 {% endif %}
	 {% endfor %}
	</dl>
{% endfor %}
