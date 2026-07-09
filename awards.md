---
layout: page
permalink: /awards/
title: Awards
lang: en
description: Awards, honors, talent programs, and competition awards of Guanbo Wang.
---

<p class="section-note">Awards and honors are organized from the provided master data. Certificate files are not published unless explicitly released.</p>

## Talent Programs and Grants

<div class="project-list">
{% for item in site.data.awards.talent_grants %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span><span>{{ item.role_en }}</span></p>
  </article>
{% endfor %}
</div>

## Academic Honors

<div class="project-list compact-list">
{% for item in site.data.awards.academic_honors %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>

## Competition Awards

<div class="project-list">
{% for item in site.data.awards.competitions %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    {% if item.project_en %}<p><strong>{{ item.project_en }}</strong></p>{% endif %}
    <p class="pub-meta">
      <span>{{ item.year }}</span>
      {% if item.role_en %}<span>{{ item.role_en }}</span>{% endif %}
      {% if item.certificate_no %}<span>Certificate No. {{ item.certificate_no }}</span>{% endif %}
    </p>
    {% if item.issuer_en %}<p class="pub-venue">{{ item.issuer_en }}{% if item.issued_date_en %}, {{ item.issued_date_en }}{% endif %}</p>{% endif %}
  </article>
{% endfor %}
</div>

## Certificates

<div class="project-list compact-list">
{% for item in site.data.awards.certificates %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>
