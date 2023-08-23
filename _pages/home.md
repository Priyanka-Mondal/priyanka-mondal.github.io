---
title: "Owen Arden"
layout: homelay
sitemap: false
permalink: /
---

### Research Interests
<br />

<img align="right" style="margin:0.5em" src="/home/images/areas.svg"/>

<p style="font-size:130%">
I study **decentralized security** with a focus on
using **programming language theory and design** to build decentralized
applications that are **secure by construction**.  My research includes both
foundational and practical contributions, from developing novel, more expressive
security models and formalized programming languages, to building secure decentralized systems
and compilers.
</p>
<br clear="right"/>

<!--
#### Advancing Computer Security Foundations
#### Designing Secure Programming Abstractions
#### Building Secure Distributed and Decentralized Systems

Developing secure applications is unreasonably hard. Real-world security breaches rarely result from direct attacks on security mechanisms. Instead, attackers take advantage of applications that use these mechanisms incorrectly or violate their assumptions.

Application developers should be domain experts, not security experts. I study language-based approaches to building decentralized and distributed applications that are secure by construction. Using high-level abstractions to synthesize low-level security protocols, programmers can build secure applications without being security experts.

-->

{% if site.data.news %}
<div class="jumbotron">
### News
{% for item in site.data.news %}
<h5><b>{{item.headline}}</b>: {{item.shorttext}}</h5> 
{% endfor %}
</div>
{% endif %}

### Recent publications
{% bibliography --query @article[year >= 2017] or @inproceedings[year >= 2017] or @techreport[year >= 2017]%}
