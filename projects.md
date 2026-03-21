---
layout: default
title: Projects
nav_title: Projects
nav_order: 6
---

<section class="page-card">
  <h1>Projects</h1>
  <p class="page-intro">I treated “Projectm” in the request as “Projects.” Rename this page if you intended a different label.</p>

  <div class="stack">
    {% for item in site.data.projects %}
      <article class="section-card">
        <p class="badge">{{ item.status }}</p>
        <h2 class="item-title">{{ item.title }}</h2>
        <p>{{ item.summary }}</p>
      </article>
    {% endfor %}
  </div>
</section>
