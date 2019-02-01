---
layout: home
---

# Overzicht API's

<table>
  <thead>
    <tr>
      <th>Titel</th>
      <th>Org.</th>
      <th>API description</th>
      <th>Formaat</th>
      <th>OASv3</th>
      <th>Valid</th>
      <th>Score</th>
    </tr>
  </thead>
  <tbody>
    {% for api in site.data.apis._embedded.apis %}
    <tr>
        <td>{{ api.title }}</td>
        <td>{{ api.organisation }}</td>
        <td>{{ api.descriptionFile }}</td>
        <td>{{ api.descriptionFormat }}</td>
        <td>{% if api.oasv3  %}<a href="oas/{{ api.oasv3 }}">{{ api.oasv3 }}</a>{% endif %}</td>
        <td>{{ api.valid }}</td>
        <td>{{ api.score }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
