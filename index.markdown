---
---
layout: default
title: "首页"
---

<div class="cards-container">
  {% for post in paginator.posts %}
    <div class="card">
      {% if post.image %}
        <img class="card-img-top" src="{{ post.image | relative_url }}" alt="{{ post.title }}">
      {% endif %}
      <div class="card-body">
        <h2 class="card-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="card-text">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
        <a href="{{ post.url | relative_url }}" class="btn">阅读全文</a>
      </div>
    </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.previous_page %}
    <a class="pagination-prev" href="{{ paginator.previous_page_path | relative_url }}">&laquo; 上一页</a>
  {% endif %}
  {% if paginator.next_page %}
    <a class="pagination-next" href="{{ paginator.next_page_path | relative_url }}">下一页 &raquo;</a>
  {% endif %}
</div>


---
