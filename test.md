# Repositories
{% for repository in site.github.public_repositories %}
  {% comment %} 
    if repository.name contains 'shell-' 
    if {{ repository.name | slice: 0,5 == 'shell' }} and {{ repository.name | slice: 6,10 >= 2015 }} and {{ repository.name | slice: 10 == '-' }}
  {% endcomment %}
  {% assign name_length = repository.name | size %}
  {% if name_length == 16 %}
    {% assign slice1 = repository.name | slice: 0,5 %}
    {% if slice1 == 'shell' %}
    * [{{ repository.name }}]({{ repository.html_url }})
    {% endif %}
  {% endif %}
{% endfor %}

--------

Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
