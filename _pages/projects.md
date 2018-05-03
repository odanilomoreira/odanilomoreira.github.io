---
title: "Projects"
layout: archive
permalink: /projects/
author_profile: true
header:
    image: "/images/banner.jpg"

---

{% include base_path %}
{% include group-by-array collection=site.posts field="categories" %}

{% for cat in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ cat | slugify }}" class="archive__subtitle">{{ cat }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}

