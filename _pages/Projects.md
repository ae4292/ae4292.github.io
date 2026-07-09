---
layout: archive
title: "Projects"
permalink: /Projects/
author_profile: false
---

{% include base_path %}

<p class="page-lead">Applied projects in machine learning, causal inference, and financial modeling.</p>

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}


