---
layout: page
permalink: /projects/
title: Projects
lang: en
description: Research projects, grants, and participated projects of Guanbo Wang.
---

<p class="section-note">Selected grants, talent programs, research projects, and participated projects. Funding and project numbers are shown only when provided in the master data.</p>

{% assign groups = "Grants and Talent Programs|Research Projects|Participated Projects" | split: "|" %}
{% for group in groups %}
  <h2>{{ group }}</h2>
  <div class="project-list">
  {% assign items = site.data.projects | where: "group", group %}
  {% for item in items %}
    <article class="project-card">
      <h2>{{ item.title_en }}</h2>
      <p><strong>{{ item.project_en }}</strong></p>
      <p class="pub-venue">
        {% if item.agency_en %}{{ item.agency_en }}{% endif %}
        {% if item.project_no %} · No. {{ item.project_no }}{% endif %}
      </p>
      <p class="pub-meta">
        {% if item.period %}<span>{{ item.period }}</span>{% endif %}
        {% if item.role_en %}<span>{{ item.role_en }}</span>{% endif %}
        {% if item.status_en %}<span>{{ item.status_en }}</span>{% endif %}
      </p>
      <div class="metric-row">
        {% if item.funding_en %}<span class="metric-badge">{{ item.funding_en }}</span>{% endif %}
        {% if item.category_en %}<span class="metric-badge">{{ item.category_en }}</span>{% endif %}
      </div>
    </article>
  {% endfor %}
  </div>
{% endfor %}
