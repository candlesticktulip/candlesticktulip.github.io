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

<!-- | Name | Link | Date | Title | Dir |  
|-------|--------|---------|
{% for page in site.pages %}  
    {% if page.url contains 'applications/' %}  
        | {{ page.name }} | {{ page.url }} | {{ page.date }} | {{ page.title }} | {{ page.dir }} |  
    {% else %}
        {% comment %}Do nothing{% endcomment %}
    {% endif %}  
{% endfor %}   -->

<table class="responsive-table table">
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Date</th>
      <th scope="col">Dir</th>
    </tr>
  </thead>
  <tbody>
    {% for page in site.pages %}
      {% if page.url contains '/applications/' %}  
        <tr>
          <td> <a href="{{ page.url }}">{{ page.name }} </td>
          <td> {{ page.date }} </td>
          <td> {{ page.dir }} </td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>