## Welcome to KAUST Supercomputing Laboratory repository

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}](https://kaust-ksl.github.io/{{ repository.name }})
  {% include_relative OTP/README.md %}
{% endfor %}

{% for folder in site.folders %}
   {{ folder.title | capitalize }}
{% endfor %}

{% for folder in site.folders %}
   {{ folder.title | capitalize }}
{% endfor %}
