---
layout: single
title: "Research"
permalink: /Research/
author_profile: false
---

<p class="page-lead">Working papers and ongoing research in asset pricing, financial econometrics, and causal inference.</p>

## Working Papers

{% assign working_papers = site.publications | where: "category", "working_paper" | sort: "date" | reverse %}
{% for paper in working_papers %}
**{{ paper.title }}**
<br>{{ paper.authors }}
<br>*{{ paper.venue }}*{% if paper.venue_date %}, {{ paper.venue_date }}{% endif -%}
{%- if paper.status %}<br><span class="paper-status">{{ paper.status }}</span>{% endif -%}
{%- if paper.paperurl or paper.slidesurl %}<br>{% if paper.paperurl %}[[Paper]]({{ paper.paperurl }}){% endif %}{% if paper.slidesurl %} [[Slides]]({{ paper.slidesurl }}){% endif %}{% endif %}

{{ paper.content }}

{% unless forloop.last %}
---
{: .research-divider}
{% endunless %}
{% endfor %}

<style>
.research-divider { margin: 1.4rem 0; border: 0; border-top: 1px solid var(--global-border-color); }
</style>
