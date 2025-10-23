---
layout: default
---

## Blog posts

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}

## Resume

**[Resume / CV]({{ prepend: site.baseurl }}/resume.pdf)**

