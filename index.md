---
layout: page
title: Tags
tagline: [vim]
---
{% include JB/setup %}


<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>

<ul class="posts">
	<!--
	{% for post in site.posts %}
		<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
	-->

	{% for post in site.posts limit:3 %}
		<div class="post"><div class="posttitle"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></div>
		<div class="date">{{ post.date | date: "%A, %B %d, %Y" }}</div>
			{{ post.content }}
		</div>
	{% endfor %}
</ul>

