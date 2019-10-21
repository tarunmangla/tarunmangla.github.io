---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{https://scholar.google.com/citations?user=IP0EwogAAAAJ&hl=en}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}


Conference Publications
-----------------------
Optimal radius for connectivity in duty-cycled wireless sensor networks ([pdf](http://academicpages.github.io/files/paper1.pdf)) \
Amitabha Bagchi, Cristina M. Pinotti, Sainyam Galhotra, **Tarun Mangla** \
In *Proceedings of the 16th ACM International Conference on Modeling, Analysis and Simulation of Wireless and Mobile Systems (MSWIM '13)* 

