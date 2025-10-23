---
layout: default
---


## Blog posts

{% for post in paginator.posts %}
* [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}


## Projects

{% for project in site.projects %}
* [{{ project.title }}]({{ project.url | prepend: site.baseurl }})
{% endfor %}


## Resume

**[Resume / CV]({{ prepend: site.baseurl }}/resume.pdf)**

