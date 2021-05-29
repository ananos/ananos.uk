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
             <div style="text-align: left; font-weight:lighter; font-size:70%;">
                <i>{{ post.date | date: "%b %Y" }}  &nbsp; {%- if post.date_end -%} &#8211; &nbsp;{{ post.date_end | date: date_format }} {%- endif -%}
		</i>
            </div>

            <small>{{ post.content }}</small>

        <!-- </a> -->
        </h4>

    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}
