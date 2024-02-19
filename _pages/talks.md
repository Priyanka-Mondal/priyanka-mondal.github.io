---
layout: archive
title: ""
permalink: news/
author_profile: true
---

{% assign alltalks = site.data.talks.main | where:'render', 'true' %}
{% for talk in alltalks -%}
- {{ talk.date }} - {{ talk.title }} - {{talk.venue}}
{% endfor %}
