---
layout: default
title: Activities
nav_title: Activities
nav_order: 5
---

<section class="page-card">
  <h1>Activities</h1>
  <p class="page-intro">Use this page for service, mentoring, invited talks, workshops, outreach, and teaching contributions.</p>

  <div class="two-column">
    <article class="section-card">
      <h2>Service</h2>
      <ul class="compact-list">
        {% for item in site.data.activities.service %}
          <li><strong>{{ item.title }}:</strong> {{ item.details }}</li>
        {% endfor %}
      </ul>
    </article>

    <article class="section-card">
      <h2>Talks</h2>
      <ul class="compact-list">
        {% for item in site.data.activities.talks %}
          <li><strong>{{ item.title }}:</strong> {{ item.details }}</li>
        {% endfor %}
      </ul>
    </article>
  </div>

  <article class="section-card">
    <h2>Teaching and Training</h2>
    <ul class="compact-list">
      {% for item in site.data.activities.teaching %}
        <li><strong>{{ item.title }}:</strong> {{ item.details }}</li>
      {% endfor %}
    </ul>
  </article>
</section>
