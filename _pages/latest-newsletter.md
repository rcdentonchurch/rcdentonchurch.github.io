---
permalink: "/news/latest/"
title: "Latest Newsletter"
---

{% for file in site.static_files %}
    {% if file.path contains "newsletters/archive/" %}
    <a href="{{file.path}}" target="_blank">{{file.name}}</a>
    {% endif %}
    {% break %}
{% endfor %}
