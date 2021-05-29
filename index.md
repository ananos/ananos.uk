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
	<div style="display: inline-block; width:40px">
            <span class="fa-stack fa-1x">
              <!-- <i class="fa fa-circle fa-stack-2x "></i>-->
              <i class="fa {{ post.icon }} fa-stack-1x fa-inverse"></i>
            </span>
	</div>

        <!--<a href="{{ post.url }}">
        </a>-->
            <span>{{ post.title }}</span>
	<small>{{ post.content }}</small>
            <!-- <small>by {{ post.author }}.</small>
            <small>published {{ post.year }}.</small>-->
        </h4>
    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}

