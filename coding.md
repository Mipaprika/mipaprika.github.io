---
layout: page
---

<ul class="article-list">
{% for post in site.categories.coding %}
<li>
	<article>
		<header>
			<h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
			<time>{{ post.date|date: "%Y-%m-%d" }}</time>
		</header>
		<div class="post">{{ post.content }}</div>
	</article>
</li>
{% endfor %}
</ul>
