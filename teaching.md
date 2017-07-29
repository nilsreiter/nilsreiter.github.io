---
layout: page
title: Taught Courses
---

{% for c in site.data.courses %}
{% assign inst=site.data.locations[c.inst] %}
{% if inst.name %}
{% else %}
{% assign inst = c.inst %}
{% endif %}

- {{c.date}}: **{{ c.title }}** at {{ inst.name }}{% if c.program %} ({{ c.program | join: ", " }}){% endif %}. {% if c.with %}Taught jointly with {{c.with | join: ", " }}.{% endif %}
{% endfor %}
