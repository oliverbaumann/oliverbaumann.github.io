---
layout: single
title: "Research and Publications"
permalink: /research/
description: "Comprehensive publication list of Oliver Baumann, including journal articles, edited volumes, proceedings, practitioner outputs, and working papers."
author_profile: true
---

My research explores how organizations adapt under complexity and uncertainty, with a focus on organizational search, organization design, behavioral strategy, and decentralized governance.

> Links: DOI badge for DOI links, Paper badge for other links.

{% assign pubs = site.data.publications %}

## Articles in Refereed Journals

{% assign journal_pubs = pubs | where: "type", "journal" | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in journal_pubs %}
{% if pub.year != current_year %}
{% assign current_year = pub.year %}
### {{ current_year }}
{% endif %}

- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. *{{ pub.venue }}*{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{% if pub.link contains "doi.org" %}<span class="ob-doi-badge">DOI</span>{% else %}<span class="ob-doi-badge ob-doi-badge--alt">Paper</span>{% endif %}</a>{% endif %}
{% if pub.notes %}
  <br><small>{{ pub.notes }}</small>
{% endif %}
{% if pub.discussed_on %}
  <br><small>Discussed on:{% for link in pub.discussed_on %} <a href="{{ link }}" target="_blank" rel="noopener noreferrer">source {{ forloop.index }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}</small>
{% endif %}
{% endfor %}

## Edited Special Issues, Books, and Book Chapters

{% assign edited_pubs = pubs | where: "type", "edited_book_chapter" | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in edited_pubs %}
{% if pub.year != current_year %}
{% assign current_year = pub.year %}
### {{ current_year }}
{% endif %}

- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. *{{ pub.venue }}*{% if pub.status %} ({{ pub.status }}){% endif %}{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{% if pub.link contains "doi.org" %}<span class="ob-doi-badge">DOI</span>{% else %}<span class="ob-doi-badge ob-doi-badge--alt">Paper</span>{% endif %}</a>{% endif %}
{% endfor %}

## Articles in Refereed Conference Proceedings

{% assign proceedings_pubs = pubs | where: "type", "proceedings" | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in proceedings_pubs %}
{% if pub.year != current_year %}
{% assign current_year = pub.year %}
### {{ current_year }}
{% endif %}

- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. *{{ pub.venue }}*{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer"><span class="ob-doi-badge ob-doi-badge--alt">Paper</span></a>{% endif %}
{% endfor %}

## Publications for Practitioners

{% assign prac_pubs = pubs | where: "type", "practitioner" | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for pub in prac_pubs %}
{% if pub.year != current_year %}
{% assign current_year = pub.year %}
### {{ current_year }}
{% endif %}

- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. *{{ pub.venue }}*{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer"><span class="ob-doi-badge ob-doi-badge--alt">Paper</span></a>{% endif %}
{% endfor %}

## Working Papers

{% assign wp_pubs = pubs | where: "type", "working_paper" %}
{% for pub in wp_pubs %}
- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}.
{% endfor %}
