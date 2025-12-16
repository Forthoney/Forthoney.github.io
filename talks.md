---
layout: page
title: "/talks"
permalink: /talks
---
{% assign talks = site.talks | reverse %}
{% for talk in talks %}
### {{ talk.title }}
##### {{ talk.date | date: "%Y %B %d" }} @ {{ talk.venue }}

{{ talk.content }}

{% assign talk_links = "" | split: "" %}

{% if talk.video %}
  {% capture video_link %}[Video]({{ talk.video }}){% endcapture %}
  {% assign talk_links = talk_links | push: video_link %}
{% endif %}

{% if talk.slides %}
  {% capture slides_link %}[Slides]({{ talk.slides }}){% endcapture %}
  {% assign talk_links = talk_links | push: slides_link %}
{% endif %}

{% endfor %}
