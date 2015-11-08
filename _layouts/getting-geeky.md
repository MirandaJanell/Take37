---
layout:      default
feedurl:     "/getting-geeky/getting-geeky.xml"
feedtitle:   Getting Geeky
twitteracct: "@GettingGeekyMJ"
fbpage:      GettingGeeky
ogimage:     http://media.take37.com/getting-geeky/GettingGeeky-1400x1400-Cropped.png
---
{% capture pagetitle %}{{ page.date | date: "%B %d, %Y" }}{% endcapture %}
{% assign episodeurl = page.link | replace: 'http://', 'http://www.podtrac.com/pts/redirect.m4a/' %}

<div class="post-container">
	<h1>Getting Geeky</h1>
	{% if pagetitle %}<h2 class="post-title">{{ pagetitle }}</h2>{% endif %}
	{% if page.subtitle %}<h3 class="post-title">{{ page.subtitle }}</h3>{% endif %}

{% if page.soundcloud %}
<div>
	<iframe src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/{{ page.soundcloud }}&amp;color=cf9334&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;visual=false&amp;show_artwork=true" class="soundcloud-player" width="100%" height="166" scrolling="no" frameborder="no"></iframe>
</div>
<noscript>
	<p class="player-container">
		<audio controls>
			<source type="audio/mpeg" src="{{ episodeurl }}">
		</audio>
	</p>
</noscript>
{% else %}
{% if page.link %}
<p class="player-container">
	<audio controls>
		<source type="audio/mpeg" src="{{ episodeurl }}">
	</audio>
</p>
{% endif %}
{% endif %}
<div class="post-content">{{ content }}</div>

<p class="post-links">
	<span><i class="fa fa-calendar"></i>&nbsp;{{ page.date | date: "%B %-d, %Y" }}</span> | <span><a href="{{ episodeurl }}"><i class="fa fa-cloud-download"></i>&nbsp;Download</a></span>
</p>
</div>