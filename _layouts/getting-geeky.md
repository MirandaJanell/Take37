---
layout: default
---
<div class="post-container">
	<h2>Getting Geeky - {{ page.date | date: "%B %d, %Y" }}</h2>
	{% if page.title %}<h3 class="post-title">{{ page.title }}</h3>{% endif %}
	{% if page.subtitle %}<h4 class="post-title">{{ page.subtitle }}</h4>{% endif %}

	<div class="post-content">{{ content }}</div>
</div>