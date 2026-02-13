---
layout: default
title: "دليل المصاريف والميزانية"
description: "خريطة دلالية شاملة لمقالات المصاريف والميزانية: مصاريف، ميزانية، مصر، المغرب، أهداف، ديون مع روابط مباشرة للمحتوى والتطبيق."
permalink: /دليل-المصاريف-والميزانية/
canonical: https://fouadshawish-png.github.io/دليل-المصاريف-والميزانية/
---

# دليل المصاريف والميزانية

هذه الصفحة هي خريطة دلالية شاملة تجمع كل المحتوى المرتبط بمحوري **المصاريف** و**الميزانية** مع المسارات المحلية (مصر/المغرب) والروابط التنفيذية المرتبطة بالأهداف والديون. الهدف أن تصل إلى المحتوى المناسب بسرعة، وتبني مسار تعلم واضح بدل التنقل العشوائي.

## 1) مصاريف

- صفحة الركيزة: [المصاريف](/المصاريف/)
- مسار البداية: [كيف تنظم مصاريفك خطوة بخطوة](/organize-monthly-expenses-step-by-step/)

<ul>
{% for post in site.posts %}
  {% if post.categories contains 'المصاريف' or post.topic == 'expense-tracking' or post.title contains 'مصاريف' or post.title contains 'الإنفاق' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## 2) ميزانية

- صفحة الركيزة: [الميزانية](/الميزانية/)
- مسار التطبيق: [الميزانية الشهرية خطوة بخطوة](/الميزانية-الشهرية-خطوة-بخطوة/)

<ul>
{% for post in site.posts %}
  {% if post.categories contains 'الميزانية' or post.topic == 'budget' or post.title contains 'ميزانية' or post.title contains 'budget' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## 3) مصر

- صفحة البلد: [مصاريف-في-مصر](/مصاريف-في-مصر/)

<ul>
{% for post in site.posts %}
  {% if post.title contains 'مصر' or post.tags contains 'مصر' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## 4) المغرب

- صفحة البلد: [الميزانية-في-المغرب](/الميزانية-في-المغرب/)

<ul>
{% for post in site.posts %}
  {% if post.title contains 'المغرب' or post.tags contains 'المغرب' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## 5) أهداف

- صفحة الأهداف: [الأهداف المالية](/goals_root/)

{% assign goals_count = 0 %}
<ul>
{% for post in site.posts %}
  {% if post.tags contains 'الادخار' or post.tags contains 'أهداف' or post.title contains 'ادخار' or post.title contains 'هدف' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% assign goals_count = goals_count | plus: 1 %}
  {% endif %}
  {% if goals_count >= 20 %}{% break %}{% endif %}
{% endfor %}
</ul>

## 6) ديون

- صفحة الديون: [دفتر الديون](/debt_root/)

<ul>
{% for post in site.posts %}
  {% if post.categories contains 'الديون' or post.topic == 'debt' or post.title contains 'دين' or post.title contains 'الديون' %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## روابط تنفيذ سريعة داخل التطبيق

- [فتح التقارير](/?route=reports)
- [فتح الميزانيات](/?route=budgets)
- [فتح الديون](/?route=debt_ledger)
- [فتح العمليات](/?route=all_transactions)
