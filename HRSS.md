---
layout: page
title: HRSS
permalink: /HRSS/
---

{% for pg in site.HRSS %}
  <h2>
    <a href="{{ pg.url }}">
      {{ pg.title }} - {{ pg.type }}
    </a>
  </h2>
  <!-- <p>{{ pg.content | markdownify }}</p> -->
{% endfor %}