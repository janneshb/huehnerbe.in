---
layout: post
title: "Posts"
permalink: /posts/
author_profile: true
---

{% include base_path %}

{% for post in site.posts reversed %}
  {% include post-single.html type="list" %}
{% endfor %}
