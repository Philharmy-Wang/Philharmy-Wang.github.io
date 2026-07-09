---
layout: page
title: 关于我
permalink: /zh/
lang: zh
description: 王冠博，面向非人灵长类行为理解的计算机视觉研究。
---

<section class="hero-section">
  <div class="hero-copy">
    <p class="eyebrow">王冠博 / Guanbo Wang</p>
    <h1 class="hero-title">面向非人灵长类行为理解的计算机视觉研究</h1>
    <p class="hero-subtitle">博士后 / 助理研究员</p>
    <p class="hero-meta">中国科学院昆明动物研究所</p>
    <div class="hero-actions">
      <a class="button-link primary" href="mailto:wgb1018@gmail.com">邮箱</a>
      <a class="button-link" href="https://scholar.google.com/citations?user=Np7b_CQAAAAJ&hl=zh-TW">Google Scholar</a>
      <a class="button-link" href="https://github.com/Philharmy-Wang">GitHub</a>
      <a class="button-link" href="/zh/cv/">简历</a>
      <a class="button-link lang-switch" href="/">English</a>
    </div>
  </div>
  <img src="/images/wangguanbo.jpg" alt="王冠博" class="profile-large">
</section>

## 简介

我是**王冠博**，现任中国科学院昆明动物研究所博士后 / 助理研究员。我的研究聚焦于面向非人灵长类行为理解的计算机视觉方法，包括猕猴视觉感知、个体识别、姿态估计、行为理解和长期多摄像头笼舍监测。

我的相关研究还覆盖轻量化目标检测、边缘部署以及多模态遥感森林火灾检测。欢迎围绕动物行为研究中的可靠视觉感知系统开展交流与合作。

## 研究兴趣

<div class="research-grid">
  <div class="research-card"><strong>非人灵长类视觉感知</strong><br>服务于灵长类观测与行为研究的视觉智能方法。</div>
  <div class="research-card"><strong>猕猴检测与个体识别</strong><br>面向遮挡、运动和笼舍环境的身份感知检测。</div>
  <div class="research-card"><strong>姿态估计与行为理解</strong><br>基于姿态线索的长期、细粒度行为分析。</div>
  <div class="research-card"><strong>长期多摄像头笼舍监测</strong><br>面向连续动物行为记录的多视角监测流程。</div>
  <div class="research-card"><strong>轻量化目标检测与边缘部署</strong><br>面向资源受限场景的高效实时模型。</div>
  <div class="research-card"><strong>多模态遥感与森林火灾检测</strong><br>面向遥感森林火灾监测的检测方法。</div>
</div>

## 代表性论文

<div class="publication-grid">
{% assign selected_pubs = site.data.publications | where: "selected", true %}
{% for pub in selected_pubs limit: 6 %}
  {% include publication-card.html pub=pub lang='zh' %}
{% endfor %}
</div>

<p><a class="button-link primary" href="/zh/publications/">更多论文</a></p>

## 近期动态

<div class="news-timeline">
{% for item in site.data.news %}
  <div class="news-item">
    <span class="news-date">{{ item.date }}</span>
    <span class="news-category">{{ item.category }}</span>
    {% if item.link and item.link != '' %}<a href="{{ item.link | replace: '/publications/', '/zh/publications/' | replace: '/awards/', '/zh/awards/' }}">{{ item.title_zh }}</a>{% else %}<span>{{ item.title_zh }}</span>{% endif %}
  </div>
{% endfor %}
</div>

## 当前研究

当前博士后阶段的研究重点包括非人灵长类视觉感知、猕猴个体识别、姿态估计与行为理解，以及长期多摄像头笼舍监测。
