---
layout: page
title: Taught Courses
---

{% for c in site.data.courses %}
- {{c.date}}: **{{ c.title }}** at {{ site.data.locations[c.inst].name }} ({{ c.program | join: ", " }}). {% if c.with %}Taught jointly with {{c.with | join: ", " }}.{% endif %}
{% endfor %}
