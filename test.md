---
layout: testlayout
---

<div style="display:block; text-align:center;">
{% assign n = site.artwork | size %}
{% assign artworks = site.artwork | sample:n %}  
{% for artwork in artworks %}
{% if artwork.frontpage %}
<a href="{{ artwork.url }}">
    <div class="tile">
        <div class="tilethumbnail">
        <img src="/assets/{{ artwork.catalogue }}-thumbnail.png"/>
        </div>
        <h4>{{ artwork.title }} ({{ artwork.year }})</h4>
    </div>
</a>
{% endif %}
{% endfor %}
</div>
