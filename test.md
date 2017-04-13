# Repositories

Blah blah blah
{% for repository in site.github.public_repositories %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 %} * [{{ repository.name }}](https://evanlinde.github.io/{{ repository.name }}) {{ repository.html_url }} 
  {% endif %}
{% endfor %}


Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
