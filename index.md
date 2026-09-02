---
layout: page
title: HR管理数字化
---

{% assign posts = site.posts %}
<ul class="post-list pl-0">
{% for post in posts limit:8 %}
  <li class="py-2">
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-meta"> | {{ post.date | date: "%Y-%m-%d" }}</span>
    {% if post.description %}
    <div class="post-excerpt mt-1 mb-2 text-muted small">
      {{ post.description }}
    </div>
    {% endif %}
  </li>
{% endfor %}
</ul>

{% if posts.size > 8 %}
<div class="mt-3">
<a href="/tags/" class="btn btn-outline-primary">点击更多查看全部文章</a>
</div>
{% endif %}
