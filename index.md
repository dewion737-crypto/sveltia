---
layout: default
title: Блог
description: Статьи об изучении английского языка
---

<div class="page-wrap">
  <div class="card">
    <h2>Статьи об английском</h2>
    <p>Практические советы, разборы тем и полезные материалы для изучения английского языка.</p>
  </div>

  <div class="posts-grid">
    {% for post in site.posts %}
    <a class="post-card" href="{{ post.url | prepend: site.baseurl }}">
      {% if post.tag %}
      <div class="post-card__tag">{{ post.tag }}</div>
      {% endif %}
      <div class="post-card__title">{{ post.title }}</div>
      {% if post.intro %}
      <div class="post-card__excerpt">{{ post.intro }}</div>
      {% endif %}
      <div class="post-card__meta">
        {% if post.author %}{{ post.author }} · {% endif %}
        {{ post.date | date: "%d.%m.%Y" }}
        {% if post.read_time %} · {{ post.read_time }}{% endif %}
      </div>
    </a>
    {% endfor %}
  </div>
</div>
