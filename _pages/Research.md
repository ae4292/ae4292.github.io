---
layout: single
title: "Research"
permalink: /Research/
author_profile: false
description: "Working papers by Adrian Enders on jump comovement in industry and ownership networks and on machine-learning outlier detection for causal inference."
---

<div class="page-divider"></div>

## Working Papers

{% assign working_papers = site.publications | where: "category", "working_paper" | sort: "date" | reverse %}
{% for paper in working_papers %}
### {{ paper.title }}
{: .paper-title}

<div class="paper-meta">
{%- if paper.authors and paper.authors != site.author.name %}<span class="paper-line">{{ paper.authors }}</span>{% endif -%}
{%- if paper.venue and paper.venue != "Working Paper" %}<span class="paper-line"><em>{{ paper.venue }}</em>{% if paper.venue_date %}, {{ paper.venue_date }}{% endif %}</span>{% endif -%}
{%- if paper.status %}<span class="paper-line paper-status">{{ paper.status }}</span>{% endif -%}
{%- if paper.paperurl or paper.slidesurl %}<span class="paper-line">{% if paper.paperurl %}<a href="{{ paper.paperurl }}" aria-label="Paper PDF: {{ paper.title }}">[Paper]</a>{% endif %}{% if paper.slidesurl %} <a href="{{ paper.slidesurl }}" aria-label="Slides: {{ paper.title }}">[Slides]</a>{% endif %}</span>{% endif -%}
</div>

<details class="paper-abstract" markdown="1">
<summary>Abstract<span class="visually-hidden">: {{ paper.title }}</span></summary>

{{ paper.content }}

</details>

{% unless forloop.last %}
---
{: .research-divider}
{% endunless %}
{% endfor %}

<style>
.research-divider { margin: 1.4rem 0; border: 0; border-top: 1px solid var(--global-border-color); }
.paper-title { margin: 0 0 0.4rem; font-size: 1.05rem; line-height: 1.35; color: var(--global-base-color); }

.paper-meta .paper-line { display: block; }
.paper-abstract { margin-top: 0.6rem; }
.paper-abstract summary { cursor: pointer; color: var(--global-base-color); font-size: 0.9rem; }
.paper-abstract summary:hover { color: var(--global-link-color-hover); }
.paper-abstract p { margin-top: 0.6rem; }
</style>
