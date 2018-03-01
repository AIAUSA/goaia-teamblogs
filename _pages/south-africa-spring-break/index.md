---
title: South Africa Spring Break
date: 2018-02-21 19:15:00 Z
pagination:
  enabled: true
  collection: south-africa-spring-break
permalink: /teamblogs/south-africa-spring-break/
---

<h1>{{ paginator.page }}</h1>
{% for post in paginator.posts %}
{% if post.url contains "index" %}
{% else %}
<h2><a href="{{post.url}}">{{ post.title }}</a></h2>
{{ post.content }}
{% endif %}
{% endfor %}

{% if paginator.total_pages > 1 %}
<ul>
  {% if paginator.previous_page %}
  <li>
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl }}">Newer</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li>
    <a href="{{ paginator.next_page_path | prepend: site.baseurl }}">Older</a>
  </li>
  {% endif %}
</ul>
{% endif %}