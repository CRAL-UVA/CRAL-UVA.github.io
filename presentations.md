---
title: Teaching
permalink: /presentations/
---

### Teaching by Semester

{% assign semesters = site.teaching | sort: 'semester' | reverse %}

<ul>
  {% for course in semesters %}
    <li>
      <a href="{{ site.baseurl }}{{ course.url }}">{{ course.semester }} - {{ course.title }}</a>
    </li>
  {% endfor %}
</ul>
