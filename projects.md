---
layout: default
title: Projects
nav_title: Projects
nav_order: 6
---

<section class="page-card">
  <h1>Projects</h1>
  <p class="page-intro">Current project areas include transcriptome analysis, pan-genome research, and OrganelleCleaner.</p>

  <div class="stack">
    {% for item in site.data.projects %}
      <article class="section-card">
        {% if item.status %}
          <p class="badge">{{ item.status }}</p>
        {% endif %}
        <h2 class="item-title">{{ item.title }}</h2>
        <p>{{ item.summary }}</p>
      </article>
    {% endfor %}
  </div>
</section>
