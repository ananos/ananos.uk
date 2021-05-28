---
layout: default
---

## About

<img class="profile-picture" src="gravatar.png">

Hi! I am Anastassios Nanos and this is my personal web page. I'm an engineer,
working on various levels of the systems software stack. In this space, you can
find more information about what I'm up to and how to contact me.

---


## Working on

<ul class="related-posts">

{% assign work_items = site.posts | where: 'work', true %}
{% for post in work_items limit:5 %}
    <li class="main-page-list">
        <h4>
        <a href="{{ post.url }}">
            <span>{{ post.title }}</span>
        </a>
            <!-- <small>by {{ post.author }}.</small>
            <small>published {{ post.year }}.</small>-->
        </h4>
    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}

