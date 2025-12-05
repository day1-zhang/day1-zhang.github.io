---
layout: page
title: 标签
permalink: /tags/
---

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
### {{ tag[0] }}
{% assign tposts = tag[1] | sort: 'date' | reverse %}
{% for post in tposts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endfor %}
{% endfor %}