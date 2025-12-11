---
layout: home
title: "المقالات"
---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
