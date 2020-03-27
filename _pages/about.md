---
title: "About"
permalink: /about/
author_profile: true
header:
  image:"/images/maletsunyane.jpg"
---

I'm from Mohale's Hoek, Lesotho and I am currently masters student in Computational Finance and Risk management at the University of Washington. I am highly interested in Systematic Investing(trend following, global macro, momentum, and more) and Data Science particularly in machine learning, explorative analysis and data visualization. In Systematic interests my interests  This Portfolio provides a some projects that interest me.

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
