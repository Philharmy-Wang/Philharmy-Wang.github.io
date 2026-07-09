---
layout: page
permalink: /publications/
title: Publications
lang: en
description: Publications by Guanbo Wang.
---

<p class="section-note"><strong>Latest verified journal metrics.</strong> Source: Google Scholar screenshot provided by the author. Unclear fields are marked as <em>To be verified</em>.</p>

## Selected Publications

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs %}
  {% include publication-card.html pub=pub lang='en' %}
{% endfor %}
</div>

## Journal Articles

<div class="publication-grid">
{% assign journal_pubs = site.data.publications | where: "publication_type", "Journal Article" %}
{% for pub in journal_pubs %}
  {% unless pub.selected %}
    {% include publication-card.html pub=pub lang='en' %}
  {% endunless %}
{% endfor %}
</div>

## Chinese Publications

<div class="publication-grid">
{% assign chinese_pubs = site.data.publications | where: "publication_type", "Chinese Publication" %}
{% for pub in chinese_pubs %}
  {% include publication-card.html pub=pub lang='en' %}
{% endfor %}
</div>

## Patents

<div class="publication-grid">
  <article class="publication-card"><h3 class="pub-title">基于无人机与改进YOLOv8目标检测算法的火灾巡检预警方法</h3><p class="pub-authors"><strong>Guanbo Wang</strong>, Li Xingyong, Hu Peng, et al.</p><p class="pub-venue">CN117409191A, 2024-01-16.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于无人机实时视频流的火灾检测方法及系统</h3><p class="pub-authors"><strong>Guanbo Wang</strong>, Bao Kunyan, Hu Peng, Ding Hongwei, Yu Yongtao, Zhu Yuanjing, Yang Jundong, Yang Zhijun, Liu Qianlin, Yang Chao, Li Yushan, Wang Zongshan.</p><p class="pub-venue">CN115631436A, 2023-01-20.</p></article>
  <article class="publication-card"><h3 class="pub-title">基于无人机与英伟达开发板的目标检测方法、系统及装置</h3><p class="pub-authors"><strong>Guanbo Wang</strong>, Ding Hongwei, Yang Zhijun, Liu Qianlin, Yang Jundong, Yang Chao.</p><p class="pub-venue">CN113902994A, 2022-01-07.</p></article>
  <article class="publication-card"><h3 class="pub-title">基于改进型YOLOv4的火焰检测方法及系统</h3><p class="pub-authors">Ding Hongwei, Xu Hang, <strong>Guanbo Wang</strong>, Hu Peng, Ma Hongwei.</p><p class="pub-venue">CN115049986A, 2022-09-13.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于改进麻雀搜索算法的机器人路径规划方法及系统</h3><p class="pub-authors">Xing Xiangrui, Duan Minglei, Wu Hairong, Hu Peng, Ding Hongwei, Yang Chao, <strong>Guanbo Wang</strong>, Jiang Xinxiu, Jing Beibei, Zhao Xingbing, Kou Qianlan.</p><p class="pub-venue">CN114460941A, 2022-05-10.</p></article>
  <article class="publication-card"><h3 class="pub-title">一种基于深度学习的智能安防系统及用于智能安防系统的深度学习方法</h3><p class="pub-authors">Yang Chao, Jing Beibei, Jiang Xinxiu, Ding Guangen, Ma Hongwei, Ding Hongwei, Xing Xiangrui, <strong>Guanbo Wang</strong>, Zhao Xingbing, Kou Qianlan, Ge Haoyang, Xu Hang, Hu Kun.</p><p class="pub-venue">CN112991671A, 2021-06-18.</p></article>
</div>

## Metrics Note

<p class="metric-note">{{ site.data.journal_metrics.verification_note_en }} DOI and publisher links are shown only when verified; otherwise a Google Scholar search link is provided.</p>
