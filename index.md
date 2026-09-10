---
layout: home
---

<p class="intro-copy">
I am a postdoc at the Wharton Department of Statistics and Data Science, advised by Yuejie Chi and Yuxin Chen.
Before joining Wharton, I was hosted at Yale University for a year.
Previously, I completed my PhD in Statistics at the University of Chicago with Cong Ma.
</p>

<p class="intro-copy">
My research studies the statistical foundations of learning from heterogeneously structured data.
Recent projects include low-rank matrix estimation with multi-view integration, ranking from pairwise comparisons beyond uniform sampling, and robust reinforcement learning.
</p>

<aside class="job-market" aria-label="Job market announcement">
  <p>I am on the U.S. and international job market for the 2026–2027 cycle.</p>
</aside>

<section id="news" aria-labelledby="news-title">
  <div class="section-head">
    <h2 id="news-title">News</h2>
  </div>
  <ul class="news-list">
    <li>
      <span class="date">Sep 2026</span>
      <span>A new <a href="https://arxiv.org/abs/2609.05617">preprint</a>! It introduces bias-corrected subspace intersection (BCSI), a method for estimating subspace structure shared between two views. It improves over existing methods like AJIVE by correcting a second-order bias.</span>
    </li>
    <li>
      <span class="date">Aug 2026</span>
      <span>New <a href="https://arxiv.org/abs/2608.06545">paper</a> on robust MDPs. We use plug-in reductions, with both span-informed and span-agnostic versions, to solve distributionally robust average-reward MDPs. We discuss their behavior compared with standard AMDPs over high- and low-tolerance regimes, and establish a matching pair of sample complexity upper and lower bounds.</span>
    </li>
  </ul>
</section>

<section id="selected-papers" class="home-publications" aria-labelledby="selected-papers-title">
      <div class="section-head">
        <h2 id="selected-papers-title">Selected Papers</h2>
        <a href="{{ '/papers' | relative_url }}">All papers</a>
      </div>

      {% assign selected_papers = site.data.papers | where: "selected", true | sort: "selected_order" %}
      {% for paper in selected_papers %}
      <article class="publication">
        <div class="venue">{{ paper.venue_short | default: paper.venue }}</div>
        <div>
          <h3>{{ paper.title }}</h3>
          <p class="authors">{{ paper.authors }}</p>
          <p class="meta">{{ paper.meta }}</p>
          <div class="paper-links">
            {% for link in paper.links %}
            <a href="{% if link.relative %}{{ link.url | relative_url }}{% else %}{{ link.url }}{% endif %}">{{ link.label }}</a>
            {% endfor %}
          </div>
        </div>
      </article>
      {% endfor %}
</section>

<section id="papers" class="home-publications" aria-labelledby="papers-title">
      <div class="section-head">
        <h2 id="papers-title">Recent Papers</h2>
        <a href="{{ '/papers' | relative_url }}">All papers</a>
      </div>

      {% for paper in site.data.papers limit: 3 %}
      <article class="publication">
        <div class="venue">{{ paper.venue_short | default: paper.venue }}</div>
        <div>
          <h3>{{ paper.title }}</h3>
          <p class="authors">{{ paper.authors }}</p>
          <p class="meta">{{ paper.meta }}</p>
          <div class="paper-links">
            {% for link in paper.links %}
            <a href="{% if link.relative %}{{ link.url | relative_url }}{% else %}{{ link.url }}{% endif %}">{{ link.label }}</a>
            {% endfor %}
          </div>
        </div>
      </article>
      {% endfor %}
</section>
