---
layout: archive
title: ""
permalink: talks/
author_profile: true
---

  <h2>Talks</h2>
{% assign alltalks = site.data.talks.main | where:'render', 'true' %}

{% for talk in alltalks -%}
- {{ talk.date }} - {{ talk.title }} - {{talk.venue}}
{% endfor %}



## Grants and Fellowships 
- Travel Grant S\&P 2023 (San Francisco, USA)
- Travel Grant for Confidential Computing 2023 (San Francisco, USA)
- Travel Grant for CSF 2022 (Haifa, Israel)
- Travel Grant for POPL 2019 (Lisbon, Portugal)
- Travel Grant for PLDI 2019 (Pheonix AZ, USA)
- Travel Grant for CSF 2019 (New Jersey, USA)
- Travel Grant IARPA Hector Meeting 2019 (Baltimore DC, USA)
- Student Grant for SoCC 2019 (Santa Cruz, USA)
- Student Grant for OPLSS Summer School 2019 (Eugene OR, USA)
- Regent's Fellowship, University of California 2018
- All India GATE Scholarship for Master's studies 2013-2015
- All India Undergrad Scholarship 2009-2012
