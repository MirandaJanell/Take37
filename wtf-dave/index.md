---
layout: default
---
{% for post in site.categories.wtf-dave %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}