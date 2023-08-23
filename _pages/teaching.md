---
title: "Teaching"
layout: gridlay
sitemap: false
permalink: /teaching/
---

{% if site.data.people %}
## Teaching

<div class="jumbotron">
### Current PhD students
<ul>
{% assign phds = site.data.people | where:"degree","Ph.D." | where:"status", "current" | sort:"name" %}
{% for student in phds %}
 <li> <a href="{{ student.url }}">{{ student.name }}</a>
 {% if student.role contains 'co-advised' %}
    ({{ student.role }})
 {% endif %}
 </li>
{% endfor %}
</ul>
</div>

{% assign postdocs = site.data.people | where:"degree","postdoc" | where:"status", "current" | sort:"name" %}
{% if postdocs != empty %}
<div class="jumbotron">
### Postdocs 
  <ul>
  {% for student in postdocs %}
   <li> <a href="{{ student.url }}">{{ student.name }}</a> </li>
  {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
### Courses
<ul>
{% assign courses = site.data.courses | sort: "number" %}
{% for course in courses %}
 <li> {{course.dept}} {{course.number}}: {{ course.name }}&nbsp;
      {% for offered in course.offerings %}
        <a href="{{ offered.url }}">{{ offered.quarter }} {{ offered.year }}</a>&nbsp;
      {% endfor %}
 </li>
{% endfor %}
</ul>
</div>
<div class="jumbotron">
### Alumni
<ul>
{% assign alumni = site.data.people | where_exp:"student", "student.role contains 'advisor'" | where_exp:"student", "student.degree == 'Ph.D.' or student.degree == 'M.S.'" | where:"status", "former" | sort:"name" %}
{% assign phds = site.data.people |  where:"status", "current" | sort:"name" %}
{% for student in alumni %}
 <li><a href="{{ student.url }}">{{ student.name }}</a>
 ({{ student.degree }}{% if student.job %}, now at {{ student.job }}{% endif %})
 {% if student.role contains 'co-advised' %}
    {{ student.role }}
 {% endif %}
 </li>
{% endfor %}
</ul>
</div>

<div class="jumbotron">
### Other advising
<ul>
{% assign students = site.data.people | where_exp:"student", "student.degree == 'B.S.' or student.role contains 'committee'" | sort:"name" %}
{% for student in students %}
 <li> <a href="{{ student.url }}">{{ student.name }}</a>
 ({{ student.degree }}{% if student.job %}, now at {{ student.job }}{% endif %})
    {{ student.role }}
 </li>
{% endfor %}
</ul>
</div>
{% endif %}
