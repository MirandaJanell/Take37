---
layout: default
---
{% capture pagetitle %}{{ page.date | date: "%B %d, %Y" }}{% endcapture %}
<div class="post-container">
	<h2>Getting Geeky</h2>
	{% if pagetitle %}<h3 class="post-title">{{ pagetitle }}</h3>{% endif %}
	{% if page.subtitle %}<h4 class="post-title">{{ page.subtitle }}</h4>{% endif %}

	<div class="post-content">{{ content }}</div>
</div>