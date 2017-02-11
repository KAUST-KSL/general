## Welcome to KAUST Supercomputing Laboratory repository

{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}](https://kaust-ksl.github.io/{{ repository.name }})
  (% include_relative https://raw.githubusercontent.com/KAUST-KSL/general/master/OTP/README.md %)
{% endfor %}
