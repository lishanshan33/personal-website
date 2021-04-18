---
layout: archive
title: "about"
permalink: /about/
author_profile: false
---

{% include base_path %}

{% for post in site.about %}
  {% include archive-single.html %}
{% endfor %}