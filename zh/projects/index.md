---
layout: page
permalink: /zh/projects/
title: 研究项目
lang: zh
description: 王冠博的科研项目、人才计划与参与项目。
---

<p class="section-note">以下展示人才计划、项目资助、主持项目与参与项目。项目编号和资助金额仅在主数据中已提供时展示。</p>

{% assign groups = "人才计划与项目资助|科研项目|参与项目" | split: "|" %}
{% for group in groups %}
  <h2>{{ group }}</h2>
  <div class="project-list">
  {% assign items = site.data.projects | where: "group_zh", group %}
  {% for item in items %}
    <article class="project-card">
      <h2>{{ item.title_zh }}</h2>
      <p><strong>{{ item.project_zh }}</strong></p>
      <p class="pub-venue">
        {% if item.agency_zh %}{{ item.agency_zh }}{% endif %}
        {% if item.project_no %} · 编号：{{ item.project_no }}{% endif %}
      </p>
      <p class="pub-meta">
        {% if item.period %}<span>{{ item.period }}</span>{% endif %}
        {% if item.role_zh %}<span>{{ item.role_zh }}</span>{% endif %}
        {% if item.status_zh %}<span>{{ item.status_zh }}</span>{% endif %}
      </p>
      <div class="metric-row">
        {% if item.funding_zh %}<span class="metric-badge">{{ item.funding_zh }}</span>{% endif %}
        {% if item.category_zh %}<span class="metric-badge">{{ item.category_zh }}</span>{% endif %}
      </div>
    </article>
  {% endfor %}
  </div>
{% endfor %}
