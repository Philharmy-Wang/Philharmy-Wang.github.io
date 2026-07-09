---
layout: page
permalink: /cv/
title: CV
lang: en
description: CV of Guanbo Wang.
---

<div class="project-card">
  <h2>{{ site.data.profile.name_en }}</h2>
  <p><strong>{{ site.data.profile.position_en }}</strong><br>{{ site.data.profile.affiliation_en }}</p>
  <p>BRID: {{ site.data.profile.brid }}<br>Email: <a href="mailto:{{ site.data.profile.email }}">{{ site.data.profile.email }}</a><br>GitHub: <a href="https://github.com/{{ site.data.profile.github }}">{{ site.data.profile.github }}</a><br>Google Scholar: <a href="{{ site.data.profile.scholar }}">Profile</a></p>
</div>

## Research Interests

<div class="research-grid">
{% for area in site.data.profile.research_areas_en %}
  <div class="research-card"><strong>{{ area }}</strong></div>
{% endfor %}
</div>

## Education

{% for item in site.data.education %}
<div class="cv-row">
  <strong>{{ item.period }}</strong>
  <span>{{ item.institution_en }}, {{ item.degree_en }}</span>
</div>
{% endfor %}

## Experience

{% for item in site.data.experience %}
<div class="cv-row">
  <strong>{{ item.period }}</strong>
  <span>{{ item.title_en }}, {{ item.organization_en }}</span>
</div>
{% endfor %}

## Selected Grants and Projects

<div class="project-list compact-list">
{% for item in site.data.projects limit: 6 %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    <p>{{ item.project_en }}</p>
    <p class="pub-meta"><span>{{ item.period }}</span><span>{{ item.role_en }}</span>{% if item.funding_en %}<span>{{ item.funding_en }}</span>{% endif %}</p>
  </article>
{% endfor %}
</div>

## Selected Publications

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs %}
  {% include publication-card.html pub=pub lang='en' %}
{% endfor %}
</div>

## Patents

<div class="project-list compact-list">
{% for patent in site.data.patents %}
  <article class="project-card">
    <h2>{{ patent.title_en }}</h2>
    <p class="pub-meta"><span>{{ patent.patent_no }}</span><span>{{ patent.status_en }}</span><span>{{ patent.date }}</span></p>
  </article>
{% endfor %}
</div>

## Awards and Honors

<div class="project-list compact-list">
{% for item in site.data.awards.academic_honors limit: 5 %}
  <article class="project-card">
    <h2>{{ item.title_en }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>
