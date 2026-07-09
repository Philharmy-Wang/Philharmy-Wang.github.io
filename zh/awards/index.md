---
layout: page
permalink: /zh/awards/
title: 奖励荣誉
lang: zh
description: 王冠博的人才计划、奖励荣誉与竞赛奖项。
---

<p class="section-note">以下奖励荣誉来自主数据整理。除非明确公开发布，否则不展示证书图片或证书文件。</p>

## 人才计划与项目资助

<div class="project-list">
{% for item in site.data.awards.talent_grants %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span><span>{{ item.role_zh }}</span></p>
  </article>
{% endfor %}
</div>

## 学术荣誉

<div class="project-list compact-list">
{% for item in site.data.awards.academic_honors %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>

## 竞赛奖励

<div class="project-list">
{% for item in site.data.awards.competitions %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    {% if item.project_zh %}<p><strong>{{ item.project_zh }}</strong></p>{% endif %}
    <p class="pub-meta">
      <span>{{ item.year }}</span>
      {% if item.role_zh %}<span>{{ item.role_zh }}</span>{% endif %}
      {% if item.certificate_no %}<span>证书编号：{{ item.certificate_no }}</span>{% endif %}
    </p>
    {% if item.issuer_zh %}<p class="pub-venue">{{ item.issuer_zh }}{% if item.issued_date_zh %}，{{ item.issued_date_zh }}{% endif %}</p>{% endif %}
  </article>
{% endfor %}
</div>

## 证书

<div class="project-list compact-list">
{% for item in site.data.awards.certificates %}
  <article class="project-card">
    <h2>{{ item.title_zh }}</h2>
    <p class="pub-meta"><span>{{ item.year }}</span></p>
  </article>
{% endfor %}
</div>
