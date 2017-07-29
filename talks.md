---
layout: page
title: Talks
---

* TOC
{:toc}

## Invited Talks

{% assign talks = site.data.talks | group_by_exp: "item", "item.date | date: '%Y'" | sort: "item" %}

{% for y in talks %} 

### {{ y.name }}

{% assign thisyear = y.items | sort: "date" | reverse %}


{% for pub in thisyear %}
{% include talk.md talk=pub %}
{% endfor %}


{% endfor %}





## (some) Conference Talks

{% assign talks = site.data.ctalks | group_by_exp: "item", "item.date | date: '%Y'" | sort: "item" %}


{% for y in talks %} 

### {{ y.name }}

{% assign thisyear = y.items | sort: "date" | reverse %}

{% for pub in thisyear %}
{% include talk.md talk=pub %}
{% endfor %}

{% endfor %}



