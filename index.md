---
layout: page
title: 毛林de随笔
tagline: [vim]
---
{% include JB/setup %}

*打小我就有一个梦想，生为地主家的儿子，家有良田千顷，终日不学无术，每天领着一帮狗奴才上街去调戏一下良家妇女。*

<ul class="tag_box inline">
  {% assign tags_list = site.tags %}  
  {% include JB/tags_list %}
</ul>

<ul class="posts">
	{% for post in site.posts limit:3 %}
		<div class="post"><div class="posttitle"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></div>
		<div class="date">{{ post.date | date: "%A, %B %d, %Y" }}</div>
			{{ post.content }}
		</div>
	{% endfor %}

	{% for post in site.posts offset:3 %}
		<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
</ul>

