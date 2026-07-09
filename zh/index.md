---
layout: page
title: 关于我
permalink: /zh/
lang: zh
description: 王冠博，面向非人灵长类行为理解的计算机视觉研究。
---

<section class="hero-section">
  <div class="hero-copy">
    <p class="eyebrow">{{ site.data.profile.name_zh }} / {{ site.data.profile.name_en }}</p>
    <h1 class="hero-title">{{ site.data.profile.positioning_zh }}</h1>
    <p class="hero-subtitle">{{ site.data.profile.position_zh }}</p>
    <p class="hero-meta">{{ site.data.profile.affiliation_zh }} · BRID: {{ site.data.profile.brid }}</p>
    <div class="hero-actions">
      <a class="button-link primary" href="mailto:{{ site.data.profile.email }}">邮箱</a>
      <a class="button-link" href="{{ site.data.profile.scholar }}">Google Scholar</a>
      <a class="button-link" href="https://github.com/{{ site.data.profile.github }}">GitHub</a>
      <a class="button-link" href="/zh/cv/">简历</a>
      <a class="button-link lang-switch" href="/">English</a>
    </div>
  </div>
  <img src="/images/wangguanbo.jpg" alt="王冠博" class="profile-large">
</section>

## 简介

{{ site.data.profile.bio_zh }}

## 研究兴趣

<div class="research-grid">
{% for area in site.data.profile.research_areas_zh limit: 8 %}
  <div class="research-card"><strong>{{ area }}</strong></div>
{% endfor %}
</div>

## 代表性论文

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs limit: 5 %}
  {% include publication-card.html pub=pub lang='zh' %}
{% endfor %}
</div>

<p><a class="button-link primary" href="/zh/publications/">更多论文</a></p>

## 近期动态

<div class="news-timeline">
{% for item in site.data.news limit: 8 %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span class="news-category">{{ item.category }}</span>
    {% assign zh_link = item.link | replace: '/publications/', '/zh/publications/' | replace: '/awards/', '/zh/awards/' | replace: '/projects/', '/zh/projects/' | replace: '/cv/', '/zh/cv/' %}
    {% if item.link and item.link != '' %}<a href="{{ zh_link }}">{{ item.title_zh }}</a>{% else %}<span>{{ item.title_zh }}</span>{% endif %}
  </div>
{% endfor %}
</div>

## 当前研究

当前研究主要面向非人灵长类动物视觉感知与行为理解，重点关注群笼猕猴场景下的个体检测、个体识别、关键点检测、跨视角一致归属、长时轨迹维持、多模态行为识别与情感状态评估等问题。
