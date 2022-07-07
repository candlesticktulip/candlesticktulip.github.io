---
title: List of accepted applications
---

{% for application in site.applications %}
  <h2>
    <a href="{{ application.url }}">
      {{ application.url }}
    </a>
  </h2>
  <p>{{ application.content | markdownify }}</p>
{% endfor %}
