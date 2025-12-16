---
layout: page
title: "/publications"
permalink: /publications
---
{% for pub in site.publications | reverse %}
### {{ pub.title }}
{{ pub.authors | join: ", " | replace: "Seong-Heon Jung", "**Seong-Heon Jung**"}}
  
*{{ pub.venue }}*, [PDF]({{ pub.link }})
{% endfor %}
