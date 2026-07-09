---
layout: page
permalink: /zh/publications/
title: 论文成果
lang: zh
description: 王冠博的论文和专利。
---

<p class="section-note"><strong>{{ site.data.journal_metrics.label_zh }}。</strong> 指标来源：{{ site.data.journal_metrics.source_note_zh }}。无法确认的信息标记为 <em>待核验 / To be verified</em>。</p>

{% assign groups = "First-author Publications|Co-authored Publications|Chinese Publications|Other Publications" | split: "|" %}
{% for group in groups %}
  <h2>{% if group == "First-author Publications" %}第一作者论文{% elsif group == "Co-authored Publications" %}合作论文{% elsif group == "Chinese Publications" %}中文论文{% else %}其他论文{% endif %}</h2>
  <div class="publication-grid">
  {% assign pubs = site.data.publications | where: "group", group %}
  {% for pub in pubs %}
    {% include publication-card.html pub=pub lang='zh' %}
  {% endfor %}
  </div>
{% endfor %}

## 发明专利

<div class="publication-grid">
{% for patent in site.data.patents %}
  <article class="publication-card">
    <h3 class="pub-title">{{ patent.title_zh }}</h3>
    <p class="pub-authors">{{ patent.authors_zh_html }}</p>
    <p class="pub-venue">{{ patent.type_zh }}，{{ patent.patent_no }}，{{ patent.date }}。状态：{{ patent.status_zh }}。</p>
  </article>
{% endfor %}
</div>

## 指标说明

<p class="metric-note">{{ site.data.journal_metrics.verification_note_zh }} 仅在已核验时显示 DOI 或 Publisher 链接；否则提供 Google Scholar 检索入口。</p>
