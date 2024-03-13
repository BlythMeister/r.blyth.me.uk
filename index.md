---
title: Home
description: "My Links"
---

## Links

<ul>
{% for item in site.pages %}
	{% assign item_crumbs = item.url | remove_first: page.dir | split: '/' %}

	{% if item_crumbs.size == 1 and item.name == 'index.md' %}
	<li>
		<a href="{{ item.url | relative_url }}">{{ item.title }}</a>
	</li>
	{% endif %}
{% endfor %}
</ul>