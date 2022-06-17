---
layout: default
---

{% include navigation.html %}

  {% for post in site.posts %}
<p><a href="{{ post.url }}">{{ post.title }}</a></p>
  {% endfor %}
