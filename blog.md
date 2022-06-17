---
layout: default
---

{% include navigation.html %}
  {% for post in site.posts %}
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.title }} {{ post.date }}</p>
  {% endfor %}
