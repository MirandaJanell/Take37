---
layout: default
---
{% for post in site.categories.suds-sunday %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}