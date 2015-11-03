---
layout: default
---
<div class="alert alert-info alert-dismissible" role="alert">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
  <strong>Disclaimer</strong> I don't have a page template for this yet, but I figure something is better than nothing.
</div>

{% for post in site.categories.getting-geeky %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}