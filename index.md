---
layout: home
---

- Totaal aantal API's: {{ site.data.apis.size }}
- Valid: 5 (83,33%)
- Invalid: 1 (16,67%)
- Swagger: 4 (66,67%)
- API Blueprint: 1 (16,67%)
- OASv3:  1 (16,67%)

<table>
  <thead>
    <tr>
      <th>Titel</th>
      <th>Organisatie</th>
      <th>Formaat</th>
      <th>OpenAPI 3.0</th>
    </tr>
  </thead>
  <tbody>
    {% for api in site.data.apis %}
    <tr>
        <td>{{ api.title }}</td>
        <td>{{ api.organisation }}</td>
        <td>{{ api.descriptionFormat }}</td>
        <td>{% if api._links.openapiYaml %}<a href="{{ api._links.openapiYaml.href }}">YAML</a> - <a href="{{ api._links.openapiJson.href }}">JSON</a>{% endif %}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
