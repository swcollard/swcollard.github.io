---
layout: page
title: Writing
permalink: /writing/
---

<h1 class="page-heading">Writing</h1>

<ul class="feed">
  {% for post in site.posts %}
  <li class="feed-item">
    <a href="{{ post.url }}">{{ post.title }}</a>
    <div class="feed-meta">{{ post.date | date: "%b %-d, %Y" }} · Post</div>
  </li>
  {% endfor %}
</ul>
