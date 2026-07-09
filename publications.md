---
layout: page
permalink: /publications/
title: Publications
lang: en
description: Publications by Guanbo Wang.
---

<p class="section-note"><strong>{{ site.data.journal_metrics.label_en }}.</strong> Source: {{ site.data.journal_metrics.source_note_en }}. Unclear fields are marked as <em>To be verified</em>.</p>

{% assign groups = "First-author Publications|Co-authored Publications|Chinese Publications|Other Publications" | split: "|" %}
{% for group in groups %}
  <h2>{% if group == "First-author Publications" %}First-author Publications{% elsif group == "Co-authored Publications" %}Co-authored Publications{% elsif group == "Chinese Publications" %}Chinese Publications{% else %}Other Publications{% endif %}</h2>
  <div class="publication-grid">
  {% assign pubs = site.data.publications | where: "group", group %}
  {% for pub in pubs %}
    {% include publication-card.html pub=pub lang='en' %}
  {% endfor %}
  </div>
{% endfor %}

## Patents

<div class="publication-grid">
{% for patent in site.data.patents %}
  <article class="publication-card">
    <h3 class="pub-title">{{ patent.title_zh }}</h3>
    <p class="pub-authors">{{ patent.authors_en_html }}</p>
    <p class="pub-venue">{{ patent.type_en }}, {{ patent.patent_no }}, {{ patent.date }}. Status: {{ patent.status_en }}.</p>
  </article>
{% endfor %}
</div>

## Metrics Note

<p class="metric-note">{{ site.data.journal_metrics.verification_note_en }} DOI and publisher links are shown only when verified; otherwise a Google Scholar search link is provided.</p>
