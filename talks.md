---
layout: page
title: "/talks"
permalink: /talks
---
{% for talk in site.talks %}
  ### {{ talk.title }}
  ##### {{ talk.date }} @ {{ talk.venue }}
  {{ talk.content }}

  {% if talk.video %}
    [Video]({{ talk.video }}),
  {% endif %}
  {% if talk.slides %}
    [Slides]({{ talk.slides }})
  {% endif %}
{% endfor %}
