---
layout: page
permalink: /zh/publications/
title: 论文成果
lang: zh
description: 王冠博的论文和专利。
---

<p class="section-note"><strong>最新核验期刊指标。</strong> 指标来源：作者提供的 Google Scholar 截图。截图中无法确认的信息标记为 <em>待核验 / To be verified</em>。</p>

## 代表性论文

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs %}
  {% include publication-card.html pub=pub lang='zh' %}
{% endfor %}
</div>

## 英文学术论文

<div class="publication-grid">
{% assign journal_pubs = site.data.publications | where: "publication_type", "Journal Article" %}
{% for pub in journal_pubs %}
  {% unless pub.selected %}
    {% include publication-card.html pub=pub lang='zh' %}
  {% endunless %}
{% endfor %}
</div>

## 中文论文

<div class="publication-grid">
{% assign chinese_pubs = site.data.publications | where: "publication_type", "Chinese Publication" %}
{% for pub in chinese_pubs %}
  {% include publication-card.html pub=pub lang='zh' %}
{% endfor %}
</div>

## 发明专利

<div class="publication-grid">
  <article class="publication-card"><h3 class="pub-title">基于无人机与改进YOLOv8目标检测算法的火灾巡检预警方法</h3><p class="pub-authors"><strong>王冠博</strong>, 李兴勇, 胡朋, 等.</p><p class="pub-venue">CN117409191A, 2024-01-16.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于无人机实时视频流的火灾检测方法及系统</h3><p class="pub-authors"><strong>王冠博</strong>, 保昆燕, 胡朋, 丁洪伟, 于勇涛, 朱元静, 杨俊东, 杨志军, 柳虔林, 杨超, 李羽珊, 王宗山.</p><p class="pub-venue">CN115631436A, 2023-01-20.</p></article>
  <article class="publication-card"><h3 class="pub-title">基于无人机与英伟达开发板的目标检测方法、系统及装置</h3><p class="pub-authors"><strong>王冠博</strong>, 丁洪伟, 杨志军, 柳虔林, 杨俊东, 杨超.</p><p class="pub-venue">CN113902994A, 2022-01-07.</p></article>
  <article class="publication-card"><h3 class="pub-title">基于改进型YOLOv4的火焰检测方法及系统</h3><p class="pub-authors">丁洪伟, 徐航, <strong>王冠博</strong>, 胡鹏, 马宏伟.</p><p class="pub-venue">CN115049986A, 2022-09-13.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于改进麻雀搜索算法的机器人路径规划方法及系统</h3><p class="pub-authors">邢湘瑞, 段明磊, 吴海蓉, 胡朋, 丁洪伟, 杨超, <strong>王冠博</strong>, 蒋欣秀, 井贝贝, 赵兴兵, 寇倩兰.</p><p class="pub-venue">CN114460941A, 2022-05-10.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于深度学习的智能安防系统及用于智能安防系统的深度学习方法</h3><p class="pub-authors">杨超, 井贝贝, 蒋欣秀, 丁广恩, 马宏伟, 丁洪伟, 邢湘瑞, <strong>王冠博</strong>, 赵兴兵, 寇倩兰, 葛昊洋, 徐航, 胡坤.</p><p class="pub-venue">CN112991671A, 2021-06-18.</p></article>
</div>

## 指标说明

<p class="metric-note">{{ site.data.journal_metrics.verification_note_zh }} 仅在已核验时显示 DOI 或 Publisher 链接；否则提供 Google Scholar 检索入口。</p>
