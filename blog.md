---
layout: default
---

{% include navigation.html %}

<div style="width:100%;">
  {% for post in site.posts %}
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p>{{ post.date | date: '%B %d, %Y'}}</p>
    <p>{{ post.teaser }}</p>
  <p><a href="{{ post.url }}">Read more...</a></p>
  {% endfor %}
</div>
<div id = "spacer" style="padding: 20px; width:100%;"></div>
