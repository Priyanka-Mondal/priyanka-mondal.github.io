---
layout: default
title: ""
permalink: news/
author_profile: false
---

{% assign allnews = site.data.somenews.main %}

{% for news in allnews -%}
|{{news.date}}|{{news.title}}|
{% endfor %}
