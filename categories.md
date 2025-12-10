---
layout: page
title: 分类
permalink: /categories/
---

## 数学
{% assign math_posts = site.categories['数学'] | sort: 'date' | reverse %}
{% if math_posts and math_posts.size > 0 %}
{% for post in math_posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endfor %}
{% else %}
暂无文章
{% endif %}

### 高等概率论
{% assign adv_prob_by_chapter = site.categories['高等概率论'] | sort: 'chapter' %}
{% assign adv_prob_by_date = site.categories['高等概率论'] | sort: 'date' | reverse %}
{% if adv_prob_by_chapter and adv_prob_by_chapter.size > 0 %}
{% for post in adv_prob_by_chapter %}
{% if post.chapter %}
- 第{{ post.chapter }}章：[{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endif %}
{% endfor %}
{% for post in adv_prob_by_date %}
{% unless post.chapter %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endunless %}
{% endfor %}
{% else %}
暂无文章
{% endif %}

## 学习理论
{% assign lt_posts = site.categories['学习理论'] | sort: 'date' | reverse %}
{% if lt_posts and lt_posts.size > 0 %}
{% for post in lt_posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endfor %}
{% else %}
暂无文章
{% endif %}

## 时序大模型
{% assign tsllm_posts = site.categories['时序大模型'] | sort: 'date' | reverse %}
{% if tsllm_posts and tsllm_posts.size > 0 %}
{% for post in tsllm_posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: '%Y-%m-%d' }}
{% endfor %}
{% else %}
暂无文章
{% endif %}
