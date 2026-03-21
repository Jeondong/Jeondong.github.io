---
layout: default
title: Contact
nav_title: Contact
nav_order: 7
---

<section class="page-card">
  <h1>Contact</h1>
  <p class="page-intro">{{ site.data.contact.message }}</p>

  <div class="two-column">
    <article class="section-card">
      <h2>Details</h2>
      <ul class="compact-list">
        <li><strong>Email:</strong> <a href="mailto:{{ site.data.contact.email }}">{{ site.data.contact.email }}</a></li>
        <li><strong>Office:</strong> {{ site.data.contact.office }}</li>
      </ul>
    </article>

    <article class="section-card">
      <h2>Profiles</h2>
      <ul class="compact-list">
        {% for item in site.data.contact.social %}
          <li><a href="{{ item.url }}">{{ item.label }}</a></li>
        {% endfor %}
      </ul>
    </article>
  </div>
</section>
