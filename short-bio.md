---
layout: default
---

## Short Bio

<ul class="related-posts">

{% assign blog_posts = site.posts | where: 'bio', true %}
{% for post in blog_posts %}
    <li class="main-page-list">
        <h4>
            <div style="display: inline-block; width: 90px">
                <small>{{ post.date | date: "%b %Y" }}</small>
            </div>
        <!-- <a href="{{ site.baseurl }}{{ post.url }}">-->
            <span>{{ post.title }} - {{ post.company }}</span>
            <small>{{ post.content }}</small>

        <!-- </a> -->
        </h4>
    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}
