---
layout: archive
permalink: /quant-finance/
title: "Quantitative Finance"
author_profile: true
excerpt: "Patterns of price movement are not random. However, they're close enough to random. -Jim Simmons "
header:
  overlay_image: "/images/data.jpeg"

---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
