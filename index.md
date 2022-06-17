---
layout: default
---

<div style="display:block; text-align:center;">
{% assign n = site.artwork | size %}
{% assign artworks = site.artwork | sample:n %}
{% for artwork in artworks %}
<a href="{{ artwork.url }}"><div style="height: 300px; width: 300px; min-width:300px; min-height:300px; display:inline-block;">
  <h4>{{ artwork.title }} ({{ artwork.year }})</h4>
  <div style="width:100%; height:250px; text-align:center;">
  <img src="/assets/{{ artwork.catalogue }}-thumbnail.png"></img>
  </div>
  </div></a>
{% endfor %}
</div>
