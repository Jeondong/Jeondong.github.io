---
layout: default
title: News
nav_title: News
nav_order: 2
---

<section class="page-card">
  <h1>News</h1>
  <p class="page-intro">Recent awards, recognitions, and funding updates.</p>

  <div class="stack">
    {% for item in site.data.news %}
      <article class="section-card">
        <p class="badge">
          {% if item.display_date %}
            {{ item.display_date }}
          {% else %}
            {{ item.date | date: "%b %-d, %Y" }}
          {% endif %}
        </p>
        <h2 class="item-title">{{ item.title }}</h2>
        <p>{{ item.details }}</p>
      </article>
    {% endfor %}
  </div>
</section>
