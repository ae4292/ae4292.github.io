---
layout: single
title: "Research"
permalink: /Research/
author_profile: false
---

## Working Papers

{% assign working_papers = site.publications | where: "category", "working_paper" | sort: "date" | reverse %}
{% for paper in working_papers %}
**{{ paper.title }}**
<br>{{ paper.authors }}
<br>*{{ paper.venue }}*{% if paper.venue_date %}, {{ paper.venue_date }}{% endif %}
{% if paper.status %}<br>*{{ paper.status }}*{% endif %}
{% if paper.paperurl or paper.slidesurl %}<br>{% if paper.paperurl %}[[Paper]]({{ paper.paperurl }}){% endif %}{% if paper.slidesurl %} [[Slides]]({{ paper.slidesurl }}){% endif %}{% if paper.slides_short_url %} [[Short Slides]]({{ paper.slides_short_url }}){% endif %}{% endif %}

{{ paper.content }}

{% unless forloop.last %}---{% endunless %}
{% endfor %}
