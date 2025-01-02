---
layout: archive
title: "Miscellaneous"
permalink: /miscellaneous/
author_profile: true
redirect_from: 
  - /miscellaneous/
  - /miscellaneous.md
---

Peer interview
====

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
