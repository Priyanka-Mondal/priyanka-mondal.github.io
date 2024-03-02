---
layout: archive
title: ""
permalink: talks/
author_profile: true
---

<h2>Talks</h2>
{% assign alltalks = site.data.talks.main | where:'render', 'true' %}

{% for talk in alltalks -%}
- {{ talk.conference }} - {{ talk.title }} - {{talk.venue}}
{% endfor %}

