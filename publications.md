---
layout: default
title: Publications
nav_title: Publications
nav_order: 3
---

<section class="page-card">
  <h1>Publications</h1>
  <p class="page-intro">Update `_data/publications.yml` with your papers, preprints, software notes, datasets, and external links.</p>

  <div class="stack">
    {% assign publications = site.data.publications | sort: "year" | reverse %}
    {% for item in publications %}
      <article class="section-card">
        <p class="badge">{{ item.year }}</p>
        <h2 class="item-title">{{ item.title }}</h2>
        <p class="item-meta">{{ item.authors }} · {{ item.venue }} · {{ item.note }}</p>
        {% if item.links %}
          <p>
            {% for link in item.links %}
              <a href="{{ link.url }}">{{ link.label }}</a>{% unless forloop.last %} · {% endunless %}
            {% endfor %}
          </p>
        {% endif %}
      </article>
    {% endfor %}
  </div>
</section>
