# Repositories
{% for repository in site.github.public_repositories %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 %}
    {% assign slice1 = repository.name | slice: 0,5 %}
    * [{{ repository.name }}]({{ repository.html_url }}) {{ slice1 }}
  {% endif %}
{% endfor %}

--------

Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
