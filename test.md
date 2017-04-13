# Repositories

Blah blah blah
{% for repository in site.github.public_repositories %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 %} 
  {% assign year = repository.name | slice: 6,10 %}
  * [{{ repository.name }}](https://evanlinde.github.io/{{ repository.name }}) {{ year }}
  {% endif %}
{% endfor %}


Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}

repository.html_url
