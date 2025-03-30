---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

---
layout: default
title: "首页"
---
<div class="card-container">
  {% for post in paginator.posts %}
  <div class="card">
    {% if post.image %}
    <!-- 如果文章 front matter 中定义了 image 字段，则显示特色图片 -->
    <img class="card-img-top" src="{{ post.image | relative_url }}" alt="{{ post.title }}">
    {% endif %}
    <div class="card-body">
      <h2 class="card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <!-- 使用 excerpt 展示文章摘要，可在文章中通过设置 excerpt_separator 控制摘要截断 -->
      <p class="card-text">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ post.url | relative_url }}" class="btn">阅读更多</a>
    </div>
  </div>
  {% endfor %}
</div>

<!-- 分页导航 -->

<div class="pagination">
  {% if paginator.previous_page %}
  <a class="pagination-prev" href="{{ paginator.previous_page_path | relative_url }}">« 上一页</a>
  {% endif %}
  {% if paginator.next_page %}
  <a class="pagination-next" href="{{ paginator.next_page_path | relative_url }}">下一页 »</a>
  {% endif %}
</div>
