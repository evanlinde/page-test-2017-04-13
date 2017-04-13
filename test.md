# Repositories
{% for repository in site.github.public_repositories %}
  {% if repository.name contains 'shell-' %}
  * [{{ repository.name }}]({{ repository.html_url }})
  {% endif %}
{% endfor %}
