---
---
<table class='table table-striped'>
  <tr>
    <th>Date</th>
    <th>Buyer</th>
    <th>Supplier</th>
    <th>Description</th>
    <th>Total Paid</th>
  </tr>
  {% for row in site.data.national.expenditure %}
    <tr>
      <td>{{row.date}}</td>
      <td><a href='{{row.buyer_url}}'>{{row.buyer}}</a></td>
      <td><a href='{{row.supplier_url}}'>{{row.supplier}}</a></td>
      <td><a href='http://www.unspsc.org/search-code/default.aspx?CSS={{row.unspsc_code}}'>{{row.description}}</a></td>
      <td>£{{row.total_paid}}</td>
    </tr>
  {% endfor %}
</table>

<a class='btn btn-primary' href='expenditure.csv'><i class='fa fa-cloud-download'></i> Download CSV</a>