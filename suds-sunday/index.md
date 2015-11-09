---
layout:   default
title:    Suds Sunday
abstract: Friends unwinding just before the start of the work week.
---
<img src="http://media.take37.com/suds-sunday/SudsSunday-360x360.png" width="360" height="360" class="img-responsive pull-right" alt="Suds Sunday Cover Art" />

Suds Sunday
===========

### Episodes

<ul>
{% for post in site.categories.suds-sunday %}
	<li>
		<h4><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
		<p class="post-links">
			<a href="{{ site.baseurl }}{{ post.url }}"><i class="fa fa-calendar"></i>&nbsp;{{ post.date | date: "%B %-d, %Y" }}</a>{% if post.link %} | <span><a href="{{ post.link | replace: 'http://', 'http://www.podtrac.com/pts/redirect.m4a/' }}"><i class="fa fa-cloud-download"></i>&nbsp;Download</a></span>{% endif %}
		</p>
	</li>
{% endfor %}
</ul>

{% for post in site.categories.suds-sunday %}
* [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}