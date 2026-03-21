---
layout: default
title: Home
nav_title: Home
nav_order: 1
---

<section class="hero">
  <div>
    <p class="badge">Plant Genomics</p>
    <h1>{{ site.data.home.headline }}</h1>
    <p>{{ site.data.profile.bio }}</p>
    <p>{{ site.data.home.summary }}</p>

    <div class="cta-row">
      <a class="button-link" href="{{ '/publications/' | relative_url }}">View Publications</a>
      <a class="button-link secondary" href="{{ '/assets/files/cv.pdf' | relative_url }}">Download CV (PDF)</a>
    </div>
  </div>

  <aside>
    <h2>At a Glance</h2>
    <ul class="hero-meta">
      <li><strong>Affiliation:</strong> {{ site.data.profile.affiliation }}</li>
      <li><strong>Location:</strong> {{ site.data.profile.location }}</li>
      <li><strong>Email:</strong> <a href="mailto:{{ site.data.profile.email }}">{{ site.data.profile.email }}</a></li>
    </ul>

    <h2>Research Interests</h2>
    <ul class="compact-list">
      {% for interest in site.data.profile.research_interests %}
        <li>{{ interest }}</li>
      {% endfor %}
    </ul>
  </aside>
</section>

<section class="two-column">
  <article class="section-card">
    <h2>Research Highlights</h2>
    <ul class="compact-list">
      {% for item in site.data.home.highlights %}
        <li><strong>{{ item.label }}:</strong> {{ item.value }}</li>
      {% endfor %}
    </ul>
  </article>

  <article class="section-card">
    <h2>Selected Links</h2>
    <ul class="compact-list">
      {% for item in site.data.profile.links %}
        <li><a href="{{ item.url }}">{{ item.label }}</a></li>
      {% endfor %}
    </ul>
  </article>
</section>

<section class="section-card">
  <h2>Recent News</h2>
  <ul class="compact-list">
    {% for item in site.data.news limit:3 %}
      <li><strong>{{ item.date | date: "%b %-d, %Y" }}</strong> · {{ item.title }}</li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/news/' | relative_url }}">Browse all news updates</a></p>
</section>
