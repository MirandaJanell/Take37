---
layout: default
---
{% for post in site.categories.getting-geeky %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}