---
layout: archive
permalink: /Data-Science/
title: "Data Science"
author_profile: true
excerpt: "All models are wrong but some are useful. - George Box"
header:
  overlay_image: "/images/data_science.jpeg"

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
