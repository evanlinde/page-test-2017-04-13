# Repositories
{% for repository in site.github.public_repositories %}
  {% comment %}{% if repository.name contains 'shell-' %}{% endcomment %}
  {% if {{ repository.name | slice: 0,5 == 'shell' }} %}
  * [{{ repository.name }}]({{ repository.html_url }})
  {% endif %}
{% endfor %}
