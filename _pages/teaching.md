---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

My teaching interests revolve around the following topics:

1. Organization theory and organization design
2. Business and corporate strategy
3. Strategy execution and performance management

I have been teaching various courses at the B.Sc., M.Sc., and executive level, at the University of Southern Denmark, the University of Munich, and the University of Strasbourg.

Currently, I am teaching the following courses:

{% include base_path %}

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}
