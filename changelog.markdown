---
layout: page
title: Changelog
permalink: /changelog/
---

<ul class="changelog-list">
  {% for post in site.posts %}
    <li class="changelog-entry">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      {% if post.excerpt %}
        {{ post.excerpt }}
      {% endif %}
    </li>
  {% endfor %}
</ul>
