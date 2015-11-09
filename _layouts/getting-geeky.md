---
layout:      default
twitteracct: "@GettingGeekyMJ"
fbpage:      GettingGeeky
---
{% capture pagetitle %}{{ page.date | date: "%B %d, %Y" }}{% endcapture %}
{% assign episodeurl = page.link | replace: 'http://', 'http://www.podtrac.com/pts/redirect.m4a/' %}

<div class="row">
	<div class="col-md-4 col-md-push-8">
		<img src="http://media.take37.com/getting-geeky/GettingGeeky-360x360.png" width="360" height="360" class="img-responsive" alt="Getting Geeky Cover Art" />
	</div>

	<div class="col-md-8 col-md-pull-4">
		<div class="post-container">
			<h1>Getting Geeky</h1>
			{% if pagetitle %}<h2 class="post-title">{{ pagetitle }}</h2>{% endif %}
			{% if page.subtitle %}<h3 class="post-title">{{ page.subtitle }}</h3>{% endif %}

		{% if page.soundcloud %}
		<div>
			<iframe src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/{{ page.soundcloud }}&amp;color=cf9334&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;visual=false&amp;show_artwork=false" class="soundcloud-player" width="100%" height="166" scrolling="no" frameborder="no"></iframe>
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
	</div>
</div>