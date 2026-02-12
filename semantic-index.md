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

{% assign expense_posts = site.posts | where_exp: "p", "p.categories contains 'المصاريف' or p.topic == 'expense-tracking' or p.title contains 'مصاريف' or p.title contains 'الإنفاق'" %}
<ul>
{% for post in expense_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## 2) ميزانية

- صفحة الركيزة: [الميزانية](/الميزانية/)
- مسار التطبيق: [الميزانية الشهرية خطوة بخطوة](/الميزانية-الشهرية-خطوة-بخطوة/)

{% assign budget_posts = site.posts | where_exp: "p", "p.categories contains 'الميزانية' or p.topic == 'budget' or p.title contains 'ميزانية' or p.title contains 'budget'" %}
<ul>
{% for post in budget_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## 3) مصر

- صفحة البلد: [مصاريف-في-مصر](/مصاريف-في-مصر/)

{% assign egypt_posts = site.posts | where_exp: "p", "p.title contains 'مصر' or p.tags contains 'مصر'" %}
<ul>
{% for post in egypt_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## 4) المغرب

- صفحة البلد: [الميزانية-في-المغرب](/الميزانية-في-المغرب/)

{% assign morocco_posts = site.posts | where_exp: "p", "p.title contains 'المغرب' or p.tags contains 'المغرب'" %}
<ul>
{% for post in morocco_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## 5) أهداف

- صفحة الأهداف: [الأهداف المالية](/goals_root/)

{% assign goals_posts = site.posts | where_exp: "p", "p.tags contains 'الادخار' or p.tags contains 'أهداف' or p.title contains 'ادخار' or p.title contains 'هدف'" %}
<ul>
{% for post in goals_posts limit:20 %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## 6) ديون

- صفحة الديون: [دفتر الديون](/debt_root/)

{% assign debt_posts = site.posts | where_exp: "p", "p.categories contains 'الديون' or p.topic == 'debt' or p.title contains 'دين' or p.title contains 'الديون'" %}
<ul>
{% for post in debt_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>

## روابط تنفيذ سريعة داخل التطبيق

- [فتح التقارير](/?route=reports)
- [فتح الميزانيات](/?route=budgets)
- [فتح الديون](/?route=debt_ledger)
- [فتح العمليات](/?route=all_transactions)
