---
layout: page
title: "/publications"
permalink: /publications
---
{% assign pubs = site.publications | reverse %}
{% for pub in pubs %}
### {{ pub.title }}
{{ pub.authors | join: ", " | replace: "Seong-Heon Jung", "**Seong-Heon Jung**"}}
  
*{{ pub.venue }}*, [PDF]({{ pub.link }})
{% endfor %}
