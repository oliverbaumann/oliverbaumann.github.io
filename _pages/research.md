---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

I am interested in *how firms’ organizational designs affect strategic outcomes such as innovation and performance*. In particular, my research focuses on two broad questions:

1. How does organization design affect a firm’s ability to deal with complex innovation problems?
2. How can firms incentivize and control innovation in complex organizations?

Theoretically, I conceive of *innovation as search and learning processes* by agents that possess only bounded rationality. In doing so, my work builds on accounts of organizational problem solving and decision making in the tradition of the behavioral theory of the firm and evolutionary economics.

Methodologically, I mainly develop formal theory through *computational models* that conceptualize *firms as complex adaptive systems*. Because such models allow studying how macro-level behavior and performance emerge from the behavior and interaction of lower-level agents (e.g., individuals, units, or firms that engage in search), they can help uncover novel mechanisms and describe the conditions under which they apply. The models I have developed either build on and extend canonical model classes or are entirely new models.

In addition to computational modeling, I have also engaged in in-depth field studies of individual firms that organize complex systems development. In other work that goes beyond the two research questions above, I have used archival data to study R&D outsourcing in the healthcare sector; I have discussed the role of organization theory for research on information systems; and I have analyzed the or-ganizational tradeoffs faced by business incubators that “assemble” new ventures.

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}


{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
