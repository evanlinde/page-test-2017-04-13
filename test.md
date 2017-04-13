# Repositories

Blah blah blah
{% for repository in site.github.public_repositories %}
  This is a line in the for loop
  {% assign name_length = repository.name | size %}
  This one comes after assigning a variable
  {% if name_length == 16 %} * [{{ repository.name }}](https://evanlinde.github.io/{{ repository.name }}) {{ repository.html_url }} 
  {% endif %}
  This is a line inside the for loop (at the end)
{% endfor %}


Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
