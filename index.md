---
layout: default
---

<div class="intro">
  <p>{{ site.description }}</p>
  <a href="https://github.com/{{ site.github_username }}">github.com/{{ site.github_username }}</a>
</div>

{% assign posts_data = "" | split: "" %}
{% for post in site.posts %}
  {% capture item %}{{ post.date | date: "%Y-%m-%d" }}|||{{ post.title }}|||{{ post.url }}|||Post{% endcapture %}
  {% assign posts_data = posts_data | push: item %}
{% endfor %}

{% assign artifacts_data = "" | split: "" %}
{% for artifact in site.data.artifacts %}
  {% capture item %}{{ artifact.date | date: "%Y-%m-%d" }}|||{{ artifact.title }}|||{{ artifact.url }}|||{{ artifact.type }}{% endcapture %}
  {% assign artifacts_data = artifacts_data | push: item %}
{% endfor %}

{% assign all_items = posts_data | concat: artifacts_data | sort | reverse %}

<ul class="feed">
  {% for item in all_items %}
    {% assign parts = item | split: "|||" %}
    <li class="feed-item">
      <a href="{{ parts[2] }}">{{ parts[1] }}</a>
      <div class="feed-meta">{{ parts[0] | date: "%b %Y" }} · {{ parts[3] }}</div>
    </li>
  {% endfor %}
</ul>
