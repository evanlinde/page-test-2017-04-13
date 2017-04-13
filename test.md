# Repositories
{% for repository in site.github.public_repositories %}
  {% comment %} 
    if repository.name contains 'shell-' 
    if {{ repository.name | slice: 0,5 == 'shell' }} and {{ repository.name | slice: 6,10 >= 2015 }} and {{ repository.name | slice: 10 == '-' }}
  {% endcomment %}
  {% capture slice1 %}{{ repository.name | slice: 0,5 }}{% endcapture %}
  {% capture year %}{{ repository.name | slice: 6,4 }}{% endcapture %}
  {% capture month %}{{ repository.name | slice: 10,2 }}{% endcapture %}
  {% capture day %}{{ repository.name | slice: 12,2 }}{% endcapture %}
  {% if slice1 == 'shell' and year >= 2015 %}
  * [{{ repository.name }}]({{ repository.html_url }})
  {% endif %}
{% endfor %}

--------

Page generated at {{ "now" | date: "%Y-%m-%d %H:%M" }}
