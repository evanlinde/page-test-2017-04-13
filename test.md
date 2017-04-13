# Repositories

Blah blah blah
{% for repository in site.github.public_repositories %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 and repository.name contains 'shell-' %} 
  {% assign d1 = repository.name | slice: 6,4 %}
  * [{{ repository.name }}](https://evanlinde.github.io/{{ repository.name }}) 
  {% endif %}
{% endfor %}


Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}

repository.html_url
