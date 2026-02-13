---
layout: single
title: "Research and Publications"
permalink: /research/
author_profile: true
---

My research explores how organizations adapt under complexity and uncertainty, with a focus on organizational search, organization design, and decentralized governance.

> Links: DOI badge for DOI links, Paper badge for other links.

{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in pubs %}
{% if pub.year != current_year %}
{% assign current_year = pub.year %}
### {{ current_year }}
{% endif %}

- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. {{ pub.venue }}{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{% if pub.link contains "doi.org" %}<span class="ob-doi-badge">DOI</span>{% else %}<span class="ob-doi-badge ob-doi-badge--alt">Paper</span>{% endif %}</a>{% endif %}
{% endfor %}
