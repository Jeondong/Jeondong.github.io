---
layout: default
title: Home
nav_title: Home
nav_order: 1
---

<section class="hero hero-profile">
  <div class="hero-visual">
    <img
      class="hero-image"
      src="{{ '/assets/images/profile-placeholder.svg' | relative_url }}"
      alt="Profile or research image for Donghyun Jeon, Ph.D."
    >
  </div>

  <div class="hero-main">
    <p class="badge">Plant Computational Genomics</p>
    <h1>Donghyun Jeon, Ph.D.</h1>
    <p class="profile-title">{{ site.data.profile.role }}</p>
    <p class="profile-affiliation">{{ site.data.profile.affiliation }}</p>
    <p class="hero-intro">{{ site.data.profile.bio }}</p>

    <div class="cta-row">
      <a class="button-link" href="{{ '/assets/files/cv.pdf' | relative_url }}">CV</a>
      <a class="button-link secondary" href="{{ '/publications/' | relative_url }}">Publications</a>
      <a class="button-link secondary" href="mailto:{{ site.data.profile.email }}">Contact</a>
      <a class="button-link secondary" href="{{ site.data.profile.website }}">Website</a>
    </div>
  </div>

  <aside class="hero-aside">
    <h2>At a Glance</h2>
    <ul class="hero-meta">
      <li><strong>Location:</strong> {{ site.data.profile.location }}</li>
      <li><strong>Email:</strong> <a href="mailto:{{ site.data.profile.email }}">{{ site.data.profile.email }}</a></li>
      <li><strong>Website:</strong> <a href="{{ site.data.profile.website }}">{{ site.data.profile.website | remove: 'https://' }}</a></li>
      <li><strong>Google Scholar:</strong> <a href="{{ site.data.profile.google_scholar }}">Profile</a></li>
      <li><strong>ORCID:</strong> <a href="{{ site.data.profile.orcid }}">0000-0002-4923-5930</a></li>
    </ul>
  </aside>
</section>

<section class="two-column research-overview">
  <article class="section-card">
    <p class="badge">Research Focus</p>
    <h2>{{ site.data.home.headline }}</h2>
    <p class="section-lead">{{ site.data.home.summary }}</p>
    <p class="section-copy">{{ site.data.home.secondary_summary }}</p>
  </article>

  <article class="section-card">
    <h2>Keywords</h2>
    <div class="keyword-grid">
      {% for topic in site.data.home.featured_topics %}
        <span class="keyword-chip">{{ topic }}</span>
      {% endfor %}
    </div>
  </article>
</section>

<section class="two-column">
  <article class="section-card">
    <h2>Selected Research Interests</h2>
    <ul class="compact-list">
      {% for interest in site.data.profile.research_interests %}
        <li>{{ interest }}</li>
      {% endfor %}
    </ul>
  </article>

  <article class="section-card">
    <h2>Selected Projects</h2>
    <ul class="compact-list">
      {% for item in site.data.projects limit:3 %}
        <li>
          <strong>{{ item.title }}</strong><br>
          {{ item.summary }}
        </li>
      {% endfor %}
    </ul>
  </article>
</section>

<section class="section-card">
  <h2>Recent News</h2>
  <ul class="compact-list">
    {% for item in site.data.news limit:3 %}
      <li>
        <strong>
          {% if item.display_date %}
            {{ item.display_date }}
          {% else %}
            {{ item.date | date: "%b %-d, %Y" }}
          {% endif %}
        </strong> · {{ item.title }}
      </li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/news/' | relative_url }}">Browse all news updates</a></p>
</section>
