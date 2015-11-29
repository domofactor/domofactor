---
layout: page
title: Archived Posts
excerpt: "An archive of posts sorted by date."
search_omit: true
---

<ul class="post-list">
{% for post in site.posts %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '<p>' | remove: '</p>' }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>