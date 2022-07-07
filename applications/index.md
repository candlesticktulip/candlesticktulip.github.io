---
title: List of accepted applications
datatable: true
---

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

<script type="text/javascript" charset="utf8" src="../src/jquery-3.6.0.min.js"></script>
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.12.1/js/jquery.dataTables.js"></script>
<script>
$(document).ready(function(){
    $('table.display').DataTable( {
        paging: true,
        stateSave: true,
        searching: true,  
        ordering: true,
        search: {
          regex: true,
          smart: true
        }
    });
});
</script>