---
layout: home
---

<p class="intro-copy">
I am a postdoc at the Wharton Department of Statistics and Data Science, advised by Yuejie Chi and Yuxin Chen.
Previously, I completed my PhD in Statistics at the University of Chicago with Cong Ma.
My work studies statistical and machine learning theory, with recent projects in matrix
estimation, ranking, reinforcement learning, and multi-matrix data analysis.
</p>

<section id="news" aria-labelledby="news-title">
  <div class="section-head">
    <h2 id="news-title">News</h2>
  </div>
  <ul class="news-list">
    <li>
      <span class="date">Jul 2026</span>
      <span>I started as a postdoc at the Wharton Department of Statistics and Data Science.</span>
    </li>
    <li>
      <span class="date">May 2026</span>
      <span>Our new preprint asks how much imperfect side information can still help in inductive matrix completion. We show that low-rank matrices can be recovered sample-efficiently even when both the observations and the side information are noisy.</span>
    </li>
  </ul>
</section>

<section id="papers" class="home-publications" aria-labelledby="papers-title">
      <div class="section-head">
        <h2 id="papers-title">Recent Papers</h2>
        <a href="{{ '/papers' | relative_url }}">All papers</a>
      </div>

      {% for paper in site.data.papers limit: 4 %}
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
