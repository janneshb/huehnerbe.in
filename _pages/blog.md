---
layout: archive
title: "Posts"
permalink: /posts/
author_profile: true
---

{% include base_path %}

What you will find here:

* Thoughts related to control and optimization
* Articles about Julia packages I developed or contributed to
* Anything I'm interested in, such as trains, photography, planes, traveling, math (...)

{% for post in site.blog reversed %}
  {% include archive-single.html type="list" %}
{% endfor %}
