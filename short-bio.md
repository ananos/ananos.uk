---
layout: default
---

## Short Bio

<ul class="related-posts">

{% assign blog_posts = site.posts | where: 'bio', true %}
{% for post in blog_posts %}
    {%- assign date_format = site.minima.date_format | default: '%b %Y' -%}
    <li class="main-page-list">
        <h4>

       <!-- <a href="{{ site.baseurl }}{{ post.url }}">-->
            <span>{{ post.company }} - {{ post.title }}</span>
             <div style="text-align: right; font-family: monospace">
                <small>{{ post.date | date: "%b %Y" }}
		{%- if post.date_end -%}
 		- {{ post.date_end | date: date_format }}
		{%- endif -%}
		</small>
            </div>

            <small>{{ post.content }}</small>

        <!-- </a> -->
        </h4>

    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}
