---
layout: default
title: pcdavid.net
---

## latest posts

<ul class="post-list">
    {% for post in site.posts %}
        {% assign currentdate = post.date | date: "%Y" %}
        {% if currentdate != date %}
            <li id="year">{{ currentdate }}</li>
        {% assign date = currentdate %}
        {% endif %}
        <li>
            <span class="post-meta">{{ post.date | date: "%B %-d" }}</span>
            <h2>
                <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
            </h2>
        </li>
    {% endfor %}
</ul>
