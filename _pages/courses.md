---
layout: archive
permalink: /courses/
title: "Relevant Courses:"
author_profile: true
---
CS 150 Data Structure and Algorithms ---
CS 202 Analysis of Algorithms


{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
