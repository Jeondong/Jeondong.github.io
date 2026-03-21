---
layout: default
title: News
nav_title: News
nav_order: 2
---

<section class="page-card">
  <h1>News</h1>
  <p class="page-intro">Use this page for time-stamped updates on manuscripts, seminars, fieldwork, datasets, awards, and milestones.</p>

  <div class="stack">
    {% for item in site.data.news %}
      <article class="section-card">
        <p class="badge">{{ item.date | date: "%b %-d, %Y" }}</p>
        <h2 class="item-title">{{ item.title }}</h2>
        <p>{{ item.details }}</p>
      </article>
    {% endfor %}
  </div>
</section>
