---
layout: page
title: About
permalink: /
lang: en
description: Guanbo Wang, computer vision for non-human primate behavior understanding.
---

<section class="hero-section">
  <div class="hero-copy">
    <p class="eyebrow">{{ site.data.profile.name_en }} / {{ site.data.profile.name_zh }}</p>
    <h1 class="hero-title">{{ site.data.profile.positioning_en }}</h1>
    <p class="hero-subtitle">{{ site.data.profile.position_en }}</p>
    <p class="hero-meta">{{ site.data.profile.affiliation_en }} · BRID: {{ site.data.profile.brid }}</p>
    <div class="hero-actions">
      <a class="button-link primary" href="mailto:{{ site.data.profile.email }}">Email</a>
      <a class="button-link" href="{{ site.data.profile.scholar }}">Google Scholar</a>
      <a class="button-link" href="https://github.com/{{ site.data.profile.github }}">GitHub</a>
      <a class="button-link" href="/cv/">CV</a>
      <a class="button-link lang-switch" href="/zh/">中文</a>
    </div>
  </div>
  <img src="/images/wangguanbo.jpg" alt="Guanbo Wang" class="profile-large">
</section>

## Short Bio

{{ site.data.profile.bio_en }}

## Research Interests

<div class="research-grid">
{% for area in site.data.profile.research_areas_en limit: 8 %}
  <div class="research-card"><strong>{{ area }}</strong></div>
{% endfor %}
</div>

## Selected Publications

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs limit: 5 %}
  {% include publication-card.html pub=pub lang='en' %}
{% endfor %}
</div>

<p><a class="button-link primary" href="/publications/">More Publications</a></p>

## Recent Updates

<div class="news-timeline">
{% for item in site.data.news limit: 8 %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span class="news-category">{{ item.category }}</span>
    {% if item.link and item.link != '' %}<a href="{{ item.link }}">{{ item.title_en }}</a>{% else %}<span>{{ item.title_en }}</span>{% endif %}
  </div>
{% endfor %}
</div>

## Current Research

Current research focuses on non-human primate visual perception and behavior understanding, especially individual detection and identification, keypoint detection, cross-view identity association, long-term trajectory maintenance, multimodal behavior recognition, and emotional state assessment in group-housed macaque scenarios.
