---
layout: default
title: Writing
---

Essays and articles on healthcare AI, machine learning, and neuroscience. New writing lands on [Substack](https://patrickmlong.substack.com/){:target="_blank"}.

<div class="articles-grid">
{% assign sorted_articles = site.articles | sort: 'date' | reverse %}
{% for article in sorted_articles %}
  {% if article.external_url %}
  <a class="article-card" href="{{ article.external_url }}" target="_blank" rel="noopener">
  {% else %}
  <a class="article-card" href="{{ article.url | relative_url }}">
  {% endif %}
      <div class="thumb-wrap">
        {% if article.thumbnail %}
        <img src="{{ article.thumbnail | relative_url }}" alt="{{ article.title }} thumbnail" loading="lazy">
        {% else %}
        <div class="thumb-placeholder">{{ article.title }}</div>
        {% endif %}
      </div>
      <div class="meta">
        <div class="title">{{ article.title }}</div>
        {% if article.date %}<div class="date">{{ article.date | date: "%B %Y" }}</div>{% endif %}
      </div>
  </a>
{% endfor %}
  <a class="article-card" href="https://patrickmlong.substack.com/p/neuroplastogens-plasticity-is-all" target="_blank" rel="noopener">
    <div class="thumb-wrap">
      <div class="thumb-placeholder">Plasticity is all you need?</div>
    </div>
    <div class="meta">
      <div class="title">Plasticity is all you need?</div>
      <div class="desc">Neuroplastogens and the role of experience in psychedelic-inspired therapies—why an open plastic window still needs the right experiential input.</div>
      <div class="date">Substack · Feb 2026</div>
    </div>
  </a>
  <a class="article-card" href="https://patrickmlong.substack.com/p/exploring-the-ways-we-review-science" target="_blank" rel="noopener">
    <div class="thumb-wrap">
      <div class="thumb-placeholder">Awaiting editor assignment</div>
    </div>
    <div class="meta">
      <div class="title">Awaiting editor assignment</div>
      <div class="desc">A tinkering reflection on peer review: a React app that renders a paper as a claims-and-evidence graph to surface my own reviewer priors.</div>
      <div class="date">Substack · Dec 2025</div>
    </div>
  </a>
</div>

[More essays on Substack →](https://patrickmlong.substack.com/){:target="_blank"}
