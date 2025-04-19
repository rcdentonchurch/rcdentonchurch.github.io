---
permalink: /about/
title: "About"
---


## Regular Masses

{% for item in site.masses %}
    {% if item.key contains "REGULAR" %}
        {% for mass in item.masses %}
            {{ mass.label }} at {{ mass.time }} on {{ mass.day }}
        {% endfor %}
    {% endif %}
{% endfor %}

## Special Masses

{% for item in site.masses %}
    {% if item.key contains "SPECIAL" %}
        {% for mass in item.masses %}
            {{ mass.label }} at {{ mass.time }} on {{ mass.day }}
        {% endfor %}
    {% endif %}
{% endfor %}

## Readings
- [Today](/readings/today/)
- [Sunday](/readings/sunday/)