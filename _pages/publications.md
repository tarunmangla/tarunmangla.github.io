---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
{% assign current_year = "" %}

{% for post in sorted_pubs %}
{% assign pub_year = post.date | date: "%Y" %}
{% if pub_year != current_year %}
{% assign current_year = pub_year %}

## {{ current_year }}

{% endif %}
<div class="publication-entry" style="margin-bottom: 1.5em;">
  <strong>{{ post.title }}</strong><br>
  {% if post.authors %}<span style="color: #555;">{{ post.authors }}</span><br>{% endif %}
  <em>{{ post.venue }}</em>{% if post.type %} <span style="background: #e8e8e8; padding: 2px 6px; border-radius: 3px; font-size: 0.85em;">{{ post.type }}</span>{% endif %}{% if post.award %} <span style="background: #ffd700; padding: 2px 6px; border-radius: 3px; font-size: 0.85em; color: #333;">{{ post.award }}</span>{% endif %}
  {% if post.paperurl %} <a href="{{ post.paperurl }}">[PDF]</a>{% endif %}
</div>
{% endfor %}
