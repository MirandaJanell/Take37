---
layout:   getting-geeky
title:    Getting Geeky
abstract: A geek culture show.
---
{% for post in site.categories.getting-geeky %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}