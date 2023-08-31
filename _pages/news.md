---
layout: default
title: ""
permalink: news/
author_profile: false
---


  <h2>News</h2>
{% assign allnews = site.data.somenews.main %}

{% for news in allnews -%}
|{{news.date}}|{{news.title}}|
{% endfor %}

[ << Back](https://priyanka-mondal.github.io/)
