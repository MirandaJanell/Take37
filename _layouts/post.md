---
layout: default
---
<div class="post-container">
	<h3 class="post-title">{{ page.title }}</h3>
	{% if page.subtitle %}<h4 class="post-title">{{ page.subtitle }}</h4>{% endif %}

	<div class="post-content">{{ content }}</div>

	<div class="post-meta">
	{% if page.categories %}
		<h4>Categories</h4>
		<ul>
		{% for cat in page.categories %}
			<li>{{ cat }}</li>
		{% endfor %}
		</ul>
	{% endif %}

	{% if page.tags %}
		<h4>Tags</h4>
		<ul>
		{% for tag in page.tags %}
			<li>{{ tag }}</li>
		{% endfor %}
		</ul>
	{% endif %}
	</div>
</div>