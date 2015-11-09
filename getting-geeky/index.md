---
layout:   default
title:    Getting Geeky
abstract: A geek culture show.
---
<img src="http://media.take37.com/getting-geeky/GettingGeeky-360x360.png" width="360" height="360" class="img-responsive pull-right" alt="Getting Geeky Cover Art" />

Getting Geeky
=============

### Episodes

<ul>
{% for post in site.categories.getting-geeky %}
	<li>
		<h4><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
		<p class="post-links">
			<a href="{{ site.baseurl }}{{ post.url }}"><i class="fa fa-calendar"></i>&nbsp;{{ post.date | date: "%B %-d, %Y" }}</a>{% if post.link %} | <span><a href="{{ post.link | replace: 'http://', 'http://www.podtrac.com/pts/redirect.m4a/' }}"><i class="fa fa-cloud-download"></i>&nbsp;Download</a></span>{% endif %}
		</p>
	</li>
{% endfor %}
</ul>