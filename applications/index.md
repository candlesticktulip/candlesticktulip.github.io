---
title: List of accepted applications
---

<!-- {% for application in site.applications %}
  <h2>
    <a href="{{ application.url }}">
      {{ application.url }}
    </a>
  </h2>
  <p>{{ application.content | markdownify }}</p>
{% endfor %} -->

| Name | Link | Date | Title | Dir |  
|-------|--------|---------|
{% for page in site.pages %}  
    {% if page.url contains 'applications/' %}  
        | {{ page.name }} | {{ page.url }} | {{ page.date }} | {{ page.title }} | {{ page.dir }} |  
    <!-- {% else %}
        {% comment %}Do nothing{% endcomment %} -->
    {% endif %}  
{% endfor %}  