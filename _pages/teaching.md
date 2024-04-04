---
layout: archive
title: ""
permalink: teaching/
author_profile: true
---

<h2>Conference Talks</h2>
{% assign alltalks = site.data.talks.main | where:'render', 'true' | where:'type', 'con'%}

{% for talk in alltalks -%}
- {{ talk.conf }} - {{ talk.title }} - {{talk.venue}}
{% endfor %}


<h2>Seminar Talks</h2>
{% assign alltalks = site.data.talks.main | where:'render', 'true' | where:'type', 'seminar'%}

{% for talk in alltalks -%}
- {{ talk.conf }} - {{ talk.title }} - {{talk.venue}}
{% endfor %}
