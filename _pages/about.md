---
permalink: /about/
title: "About"
---


## Regular Masses

{% for item in site.masses %}
    {% if item.key contains "regular_mass" %}
        {% for mass in item.masses %}
            {{ mass.label }} at {{ mass.time }} on {{ mass.day }}
        {% endfor %}
    {% endif %}
{% endfor %}

## Special Masses

{% for item in site.masses %}
    {% if item.key contains "special_mass" %}
        {% for mass in item.masses %}
            {{ mass.label }} at {{ mass.time }} on {{ mass.day }}
        {% endfor %}
    {% endif %}
{% endfor %}