---
---

# Something New Finances

This site lists finance data for Something New, all as Open Data. Pick an area below:

<table class='table table-striped'>
  <tr>
    <td>National</td>
    <td><a href='national/expenditure.html'>Expenditure</a></td>
    <td><a href='http://csvlint.io/validation/5460195963737674e3010000'><img src="http://csvlint.io/validation/5460195963737674e3010000.svg" alt="CSV Validation" /></a></td>
  </tr>
  <tr>
    <td>Horsham</td>
    <td><a href='horsham/expenditure.html'>Expenditure</a></td>
    <td><a href='http://csvlint.io/validation/545c0a1363737645490a0000'><img src="http://csvlint.io/validation/545c0a1363737645490a0000.svg" alt="CSV Validation" /></a></td>
  </tr>
</table>


## Expenditure schema

<table class='table table-striped'>
  <tr>
    <th>
      ID
    </th>
    <th>
      Title
    </th>
    <th>
      Description
    </th>
    <th>
      Type
    </th>
    <th>
      Required
    </th>
  </tr>
  {% for field in site.data.datapackage.schemas.expenditure.fields %}
    <tr>
      <td>
        {{field.name}}
      </td>
      <td>
        {{field.title}}
      </td>
      <td>
        {{field.description}}
      </td>
      <td>
        {{field.constraints.type | split:'#' | last }}
      </td>
      <td>
        {{field.constraints.required}}
      </td>
    </tr>
  {% endfor %}
</table>

<a class='btn btn-primary' href='datapackage.json'><i class='fa fa-cloud-download'></i> Download Datapackage JSON</a>