---
layout: default
---


## Posts

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}



## Resume

[resume / cv]({{ prepend: site.baseurl }}/resume.pdf)

