# Repositories
{% for repository in site.github.public_repositories %}
  {% comment %} 
    if repository.name contains 'shell-' 
    if {{ repository.name | slice: 0,5 == 'shell' }} and {{ repository.name | slice: 6,10 >= 2015 }} and {{ repository.name | slice: 10 == '-' }}
  {% endcomment %}
  {% if repository.name | slice: 0,5 == 'shell' and repository.name | slice: 10 == '-' %}
  * [{{ repository.name }}]({{ repository.html_url }})
  {% endif %}
{% endfor %}

--------

Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
