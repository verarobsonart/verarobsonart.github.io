---
layout: default
---
<style>
    .clearfix::after {
    content: <ul><li>Reference</li></ul>;
}
</style>

<div style="display:block; text-align:center;">
{% for item in site.data.navigation.toc %}
    <div style="display:inline-block; margin: 5px 20px;"><h4>{{ item.title }}</h4></div>
  {% endfor %}
</div>

<div style="display:block; text-align:center;">
{% assign n = site.artwork | size %}
{% assign artworks = site.artwork | sample:n %}
{% for artwork in artworks %}
<a href="{{ artwork.url }}">
    <div style="height: 300px; width: 300px; min-width:300px; min-height:300px; display:inline-block;">
        <h4>{{ artwork.title }} ({{ artwork.year }})</h4>
        <div style="width:100%; height:250px; text-align:center;">
        <img src="/assets/{{ artwork.catalogue }}-thumbnail.png"/>
        </div>
    </div>
</a>
{% endfor %}
</div>
