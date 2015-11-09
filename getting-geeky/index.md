---
layout:   default
title:    Getting Geeky
abstract: A geek culture show.
---
<div class="row">
	<div class="col-md-4 col-md-push-8">
		<img src="http://media.take37.com/getting-geeky/GettingGeeky-360x360.png" width="360" height="360" class="img-responsive" alt="Getting Geeky Cover Art" />
	</div>

	<div class="col-md-8 col-md-pull-4">
		<h1>Getting Geeky</h1>
		<h2>Episodes</h2>
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
	</div>
</div>