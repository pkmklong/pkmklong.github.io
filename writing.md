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
        {% if article.description %}<div class="desc">{{ article.description }}</div>{% endif %}
        {% if article.date %}<div class="date">{{ article.date | date: "%B %Y" }}</div>{% endif %}
      </div>
  </a>
{% endfor %}
</div>

[More essays on Substack →](https://patrickmlong.substack.com/){:target="_blank"}
