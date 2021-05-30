---
layout: default
---

## About

<img class="profile-picture" src="gravatar.png">

Hi! I am a systems engineer, working on various levels of the software stack.
In this space, you can find more information about the projects I am currently
working on and how to contact me.<br/>

---

## Current projects

<ul class="related-posts">

{% assign work_items = site.posts | where: 'work', true %}
{% for post in work_items limit:5 %}
    <li class="main-page-list">
        <h4>
	<div style="display: inline-block; width:40px">
            <span class="fa-stack fa-1x">
              <!-- <i class="fa fa-circle fa-stack-2x "></i>-->
              <i class="fa {{ post.icon }} fa-stack-1x "></i>
            </span>
	</div>

        <!--<a href="{{ post.url }}">
        </a>-->
            <span>{{ post.title }}</span>
	{{ post.content }}
            <!-- <small>by {{ post.author }}.</small>
            <small>published {{ post.year }}.</small>-->
        </h4>
    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}

