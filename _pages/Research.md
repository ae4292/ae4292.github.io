---
layout: single
title: "Research"
permalink: /Research/
author_profile: false
---

<div class="page-divider"></div>

## Working Papers

{% assign working_papers = site.publications | where: "category", "working_paper" | sort: "date" | reverse %}
{% for paper in working_papers %}
### {{ paper.title }}
{: .paper-title}

{{ paper.authors }}
<br>*{{ paper.venue }}*{% if paper.venue_date %}, {{ paper.venue_date }}{% endif -%}
{%- if paper.status %}<br><span class="paper-status">{{ paper.status }}</span>{% endif -%}
{%- if paper.paperurl or paper.slidesurl %}<br>{% if paper.paperurl %}[[Paper]]({{ paper.paperurl }}){% endif %}{% if paper.slidesurl %} [[Slides]]({{ paper.slidesurl }}){% endif %}{% endif %}

<details class="paper-abstract" markdown="1">
<summary>Abstract</summary>

{{ paper.content }}

</details>

{% unless forloop.last %}
---
{: .research-divider}
{% endunless %}
{% endfor %}

<style>
.research-divider { margin: 1.4rem 0; border: 0; border-top: 1px solid var(--global-border-color); }
.paper-title { margin: 0 0 0.5rem; font-size: 1.15rem; line-height: 1.35; color: var(--global-base-color); }

.paper-abstract { margin-top: 0.6rem; }
.paper-abstract summary { cursor: pointer; color: var(--global-base-color); font-size: 0.9rem; }
.paper-abstract summary:hover { color: var(--global-link-color-hover); }
.paper-abstract p { margin-top: 0.6rem; }
</style>
