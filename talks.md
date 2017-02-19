---
layout: page
title: Invited Talks
---

{% assign talks = site.data.talks | sort: "date" | reverse %}
{% for talk in talks %}

{% assign inst=site.data.locations[talk.institution] %}

{% if inst.name %}
{% else %}
{% assign inst = talk.institution %}
{% endif %}


- **{{ talk.title }}**{% if talk.with %}, with {{ talk.with }}{% endif %}. {% if talk.venue.link %}[{{ talk.venue.label }}]({{talk.venue.link}}){% else %}{{ talk.venue.label }}{% endif %} at {{inst.name}}{% if inst.country %}, {{inst.country}}{%endif%} on {{ talk.date | date: "%B %e, %Y" }}.

{% endfor %}
