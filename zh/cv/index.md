---
layout: page
permalink: /zh/cv/
title: 简历
lang: zh
description: 王冠博的简历。
---

<div class="project-card">
  <h2>{{ site.data.profile.name_zh }}</h2>
  <p><strong>{{ site.data.profile.position_zh }}</strong><br>{{ site.data.profile.affiliation_zh }}</p>
  <p>BRID：{{ site.data.profile.brid }}<br>邮箱：<a href="mailto:{{ site.data.profile.email }}">{{ site.data.profile.email }}</a><br>GitHub：<a href="https://github.com/{{ site.data.profile.github }}">{{ site.data.profile.github }}</a><br>Google Scholar：<a href="{{ site.data.profile.scholar }}">个人主页</a></p>
</div>

## 研究方向

<div class="research-grid">
{% for area in site.data.profile.research_areas_zh %}
  <div class="research-card"><strong>{{ area }}</strong></div>
{% endfor %}
</div>

## 教育经历

{% for item in site.data.education %}
<div class="cv-row">
  <strong>{{ item.period }}</strong>
  <span>{{ item.institution_zh }}，{{ item.degree_zh }}</span>
</div>
{% endfor %}

## 工作经历

{% for item in site.data.experience %}
<div class="cv-row">
  <strong>{{ item.period_zh }}</strong>
  <span>{{ item.organization_zh }}，{{ item.title_zh }}</span>
</div>
{% endfor %}

## 代表项目

<div class="project-list compact-list">
{% for item in site.data.projects limit: 6 %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    <p>{{ item.project_zh }}</p>
    <p class="pub-meta"><span>{{ item.period }}</span><span>{{ item.role_zh }}</span>{% if item.funding_zh %}<span>{{ item.funding_zh }}</span>{% endif %}</p>
  </article>
{% endfor %}
</div>

## 代表论文

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs %}
  {% include publication-card.html pub=pub lang='zh' %}
{% endfor %}
</div>

## 专利

<div class="project-list compact-list">
{% for patent in site.data.patents %}
  <article class="project-card">
    <h2>{{ patent.title_zh }}</h2>
    <p class="pub-meta"><span>{{ patent.patent_no }}</span><span>{{ patent.status_zh }}</span><span>{{ patent.date }}</span></p>
  </article>
{% endfor %}
</div>

## 奖励荣誉

<div class="project-list compact-list">
{% for item in site.data.awards.academic_honors limit: 5 %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>
