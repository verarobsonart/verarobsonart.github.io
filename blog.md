---
layout: default
---

{% include navigation.html %}

  {% for post in site.posts %}
    <a href="{{ post.url }}"><div>
    <h3>{{ post.title }}</h3>
    <p>{{ post.title }}</p>
    </a>
    </div>
  {% endfor %}
