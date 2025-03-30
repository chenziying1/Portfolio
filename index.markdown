---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
layout: home
title: "My Portfolio"
---------------------

## Featured Projects

{% for post in site.posts limit:5 %}

- [{{ post.title }}]({{ post.url }}) - {{ post.description }}
  {% endfor %}

[View all projects](/projects/)

---
