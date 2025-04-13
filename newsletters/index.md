---
title: "Newsletters"
layout: single
# author_profile: true
---

{% for file in site.static_files %}
    {% if file.path contains "newsletters/archive/" %}
<a href="{{file.path}}" target="_blank">{{file.name}}</a>
    {% endif %}
{% endfor %}