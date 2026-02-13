---
permalink: /
title: "About"
excerpt: "Professor of Strategy and Organization Design"
description: "Oliver Baumann is Professor of Strategy and Organization Design at the University of Southern Denmark, researching organizational adaptation, AI, and decentralized governance."
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am a Professor of Strategy and Organization Design at the [University of Southern Denmark (SDU)](https://www.sdu.dk), where I lead the [Strategic Organization Design](http://www.sod-research.com) research unit at the Department of Business and Management. I am also affiliated with the [Digital Democracy Center](https://www.sdu.dk/ddc).

My research examines the architecture of adaptation: how organizations design structures and decision processes to learn and innovate under uncertainty. I combine computational modeling (including NK landscapes and reinforcement learning), experiments, field studies, and digital trace data to understand how formal design interacts with behavior.

<div class="ob-callout">
<strong>Download CV:</strong> <a href="/files/Oliver_Baumann_CV_December2025.pdf">Oliver Baumann CV (December 2025)</a>
</div>

## Research Areas

<div class="ob-grid">
  <div class="ob-card">
    <h3>Performance Feedback and Search</h3>
    <p>How social comparison, aspiration levels, and self-enhancement shape exploration, adaptation, and innovation outcomes.</p>
  </div>
  <div class="ob-card">
    <h3>Organization Design in Human-AI Systems</h3>
    <p>How decision rights, hierarchy, and coordination evolve when algorithmic systems influence managerial judgment.</p>
  </div>
  <div class="ob-card">
    <h3>Decentralized Organizing</h3>
    <p>How coordination emerges in DAOs and other networked structures where authority is partially replaced by code.</p>
  </div>
</div>

## Roles and Service

- Co-Editor, [Journal of Organization Design](https://www.springer.com/journal/41469)
- Editorial boards: *Academy of Management Discoveries*, *Organization Science*, *Strategic Management Journal*

## Recent Publications

{% assign recent_pubs = site.data.publications | where: "type", "journal" | sort: "year" | reverse %}
{% for pub in recent_pubs limit: 5 %}
- **{{ pub.title }}**{% if pub.authors %} ({{ pub.authors }}){% endif %}. {{ pub.venue }}{% if pub.link %} <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{% if pub.link contains "doi.org" %}<span class="ob-doi-badge">DOI</span>{% else %}<span class="ob-doi-badge ob-doi-badge--alt">Paper</span>{% endif %}</a>{% endif %}
{% endfor %}

[See full publication list](/research/)

## Education

- PhD in Business Economics, LMU Munich
- MS in Industrial Engineering and Management, Karlsruhe Institute of Technology
- MS in Engineering Management, Portland State University

Before joining SDU, I was an Assistant Professor at LMU Munich and a Visiting Scholar at the Wharton School, University of Pennsylvania.
