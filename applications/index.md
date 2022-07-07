---
title: List of accepted applications
datatable: true
---
<script>
$(document).ready(function(){

    $('table.display').DataTable( {
        paging: true,
        stateSave: true,
        searching: true
    }
        );
});
</script>

<table class="display">
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
          <td> <a href="{{ page.url }}">{{ page.name }}</a></td>
          <td> {{ page.date }} </td>
          <td> {{ page.dir }} </td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>