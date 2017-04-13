# Repositories
{% for repository in site.github.public_repositories %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 %}
    * [{{ repository.name }}]({{ repository.html_url }}) {{ repository.tagline }} 
  {% endif %}
{% endfor %}

--------

Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
