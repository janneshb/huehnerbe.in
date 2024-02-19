---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% if site.author.googlescholar %}
  You can also find my articles on <u><a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<div class="grid__wrapper">
{% for post in site.publications reversed %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</div>
