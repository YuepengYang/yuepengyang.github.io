---
layout: page
title: "Papers"
permalink: /papers
---

<div class="page-head">
  <p class="eyebrow">Papers</p>
  <h1>Publications and Preprints</h1>
  <p>A complete list of current papers, with links to arXiv, proceedings, publishers, and slides where available.</p>
</div>

{% for paper in site.data.papers %}
<article class="publication">
  <div class="venue">{{ paper.venue }}</div>
  <div>
    <h3>{{ paper.title }}</h3>
    <p class="authors">{{ paper.authors }}</p>
    <p class="meta">{{ paper.meta }}</p>
    <div class="links">
      {% for link in paper.links %}
      <a href="{% if link.relative %}{{ link.url | relative_url }}{% else %}{{ link.url }}{% endif %}">{{ link.label }}</a>
      {% endfor %}
    </div>
  </div>
</article>
{% endfor %}
