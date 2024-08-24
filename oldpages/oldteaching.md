---
layout: archive
title: ""
permalink: teaching/
author_profile: true
---

<h2>Courses taught at University of California, Santa Cruz</h2>
{% assign allclasses = site.data.teaching.main | where:'render', 'true' %}

{% for class in allclasses -%}
- {{ class.course }} - {{ class.name }} - {{class.quarter}},  {{class.designation}}  
	With Prof. {{class.prof | newline_to_br }}  
	{{class.description | newline_to_br }}
{% endfor %}

