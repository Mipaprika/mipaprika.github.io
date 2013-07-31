---
layout: page
---

<ul>
	{% for post in site.categories.coding %}
		<li>
      <article>
		    <header>
          <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
        </header>
		    <div class="title-desc">{{ post.description }}</div>
      </article>  
		</li>
	{% endfor %}
</ul>