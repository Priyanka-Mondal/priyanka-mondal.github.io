---
layout: archive
title: ""
permalink: teaching/
author_profile: true
---

<h2>Conference Talks</h2>
{% assign alltalks = site.data.teaching.main | where:'render', 'true' | where:'type', 'con'%}

{% for talk in alltalks -%}
- {{ talk.course }} - {{ talk.name }} - {{talk.quarter}} - {{talk.designation}}
    {{talk.description}}
{% endfor %}

