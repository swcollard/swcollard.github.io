---
layout: page
title: Artifacts
permalink: /artifacts/
---

<h1 class="page-heading">Artifacts</h1>

<ul class="feed">
  {% assign sorted_artifacts = site.data.artifacts | sort: "date" | reverse %}
  {% for artifact in sorted_artifacts %}
  <li class="feed-item">
    <a href="{{ artifact.url }}">{{ artifact.title }}</a>
    <div class="feed-meta">{{ artifact.date | date: "%b %Y" }} · {{ artifact.type }}</div>
  </li>
  {% endfor %}
</ul>
