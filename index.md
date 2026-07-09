---
layout: page
title: About
permalink: /
lang: en
description: Guanbo Wang, computer vision for non-human primate behavior understanding.
---

<section class="hero-section">
  <div class="hero-copy">
    <p class="eyebrow">Guanbo Wang / 王冠博</p>
    <h1 class="hero-title">Computer Vision for Non-human Primate Behavior Understanding</h1>
    <p class="hero-subtitle">Postdoctoral Researcher / Assistant Research Fellow</p>
    <p class="hero-meta">Kunming Institute of Zoology, Chinese Academy of Sciences</p>
    <div class="hero-actions">
      <a class="button-link primary" href="mailto:wgb1018@gmail.com">Email</a>
      <a class="button-link" href="https://scholar.google.com/citations?user=Np7b_CQAAAAJ&hl=zh-TW">Google Scholar</a>
      <a class="button-link" href="https://github.com/Philharmy-Wang">GitHub</a>
      <a class="button-link" href="/cv/">CV</a>
      <a class="button-link lang-switch" href="/zh/">中文</a>
    </div>
  </div>
  <img src="/images/wangguanbo.jpg" alt="Guanbo Wang" class="profile-large">
</section>

## Short Bio

I am **Guanbo Wang**, a Postdoctoral Researcher / Assistant Research Fellow at the **Kunming Institute of Zoology, Chinese Academy of Sciences**. My research develops computer vision methods for non-human primate visual perception, macaque individual identification, pose estimation, behavior understanding, and long-term multi-camera monitoring.

My broader work also includes lightweight object detection, edge deployment, and multimodal remote sensing for wildfire detection. I welcome academic collaboration around reliable visual perception systems for animal behavior research.

## Research Interests

<div class="research-grid">
  <div class="research-card"><strong>Non-human Primate Visual Perception</strong><br>Visual AI methods for primate observation and behavioral research.</div>
  <div class="research-card"><strong>Macaque Detection and Individual Identification</strong><br>Identity-aware detection under occlusion, motion, and cage environments.</div>
  <div class="research-card"><strong>Pose Estimation and Behavior Understanding</strong><br>Pose-driven analysis for long-term, fine-grained behavior observation.</div>
  <div class="research-card"><strong>Long-term Multi-camera Cage Monitoring</strong><br>Multi-view pipelines for continuous animal behavior recording.</div>
  <div class="research-card"><strong>Lightweight Object Detection and Edge Deployment</strong><br>Efficient real-time models for resource-constrained deployment.</div>
  <div class="research-card"><strong>Multimodal Remote Sensing and Wildfire Detection</strong><br>Detection methods for remote sensing wildfire monitoring.</div>
</div>

## Selected Publications

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs limit: 6 %}
  {% include publication-card.html pub=pub lang='en' %}
{% endfor %}
</div>

<p><a class="button-link primary" href="/publications/">More Publications</a></p>

## Recent Updates

<div class="news-timeline">
{% for item in site.data.news %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span class="news-category">{{ item.category }}</span>
    {% if item.link and item.link != '' %}<a href="{{ item.link }}">{{ item.title_en }}</a>{% else %}<span>{{ item.title_en }}</span>{% endif %}
  </div>
{% endfor %}
</div>

## Current Research

My current postdoctoral research focuses on non-human primate visual perception, macaque individual identification, pose estimation and behavior understanding, and long-term multi-camera cage monitoring.
