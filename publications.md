---
layout: page
title: "/publications"
permalink: /publications
---
{% assign pubs = site.publications | reverse %}
{% for pub in pubs %}
### {{ pub.title }}
{% assign rendered_authors = "" | split: "" %}
{% assign equal_count = 0 %}
{% for author in pub.authors %}
  {% assign marker = author | slice: -1, 1 %}
  {% assign clean_author = author | remove: "*" | strip %}
  {% assign display_author = clean_author %}

  {% if clean_author == "Seong-Heon Jung" %}
    {% assign display_author = "**Seong-Heon Jung**" %}
  {% endif %}

  {% if marker == "*" %}
    {% assign equal_count = equal_count | plus: 1 %}
    {% assign display_author = display_author | append: "<sup>*</sup>" %}
  {% endif %}

  {% assign rendered_authors = rendered_authors | push: display_author %}
{% endfor %}
{{ rendered_authors | join: ", " }}
  
{% assign venue_short = pub.venue | split: "(" | last | remove: ")" | strip %}
*<span title="{{ pub.venue }}" style="cursor: help;">{{ venue_short }}</span>*
{%- if pub.link -%}
  , [PDF]({{ pub.link }})
{%- endif -%}
{% endfor %}

<sup>*</sup> Equal contribution.

