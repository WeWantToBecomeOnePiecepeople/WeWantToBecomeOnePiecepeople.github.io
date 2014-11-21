---
layout: page
title: 攻城狮's House
tagline: '我来了！' 
---
{% include JB/setup %}

{% for page in site.categories.life limit: 1 %}
<header class="post-header">
<h1><a href="{{ page.url }}">{{ page.title }}</a></h1>
<p class="meta"><i class="fa fa-calendar"></i> {{ page.date | date: "%Y-%m-%d" }}   <i class="fa fa-folder-open"></i>{% if page.category %} <a href="/categories/#{{page.category}}">{{ page.category }}</a> {% endif %}   <i class="fa fa-tags"></i> {% for tag in page.tags %} <a href="/tags/#{{ tag }}">{{ tag }}</a>{% endfor %}</p>
</header>
<article class="post-content">
{{ page.content }}
</article>
{% endfor %}


##Here's 岁月's精华.

<ul class="posts">
{% for post in site.posts %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>



