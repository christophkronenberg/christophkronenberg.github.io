---
layout: default
title: Workshop archive
permalink: /workshop/archive/
description: Past editions of the Economics of Mental Health Workshop, 2018 to 2026.
---

{% assign editions = site.data.emhw %}
{% for e in editions %}
<section class="edition" id="emhw-{{ e.year }}">
  <h2>{{ e.year }} · {{ e.place }}</h2>
  {% if e.host %}<p class="meta">Host: {{ e.host }}</p>{% endif %}
  <p><strong>Keynotes:</strong> {{ e.keynotes }}</p>
  {% if e.note %}<p>{{ e.note }}</p>{% endif %}
  {% if e.roundup %}<p><a href="{{ e.roundup }}">Meeting round-up</a></p>{% endif %}
  <a href="{{ '/assets/img/emhw/emhw-' | append: e.year | append: '.jpg' | relative_url }}"><img src="{{ '/assets/img/emhw/emhw-' | append: e.year | append: '.jpg' | relative_url }}" alt="Call for papers, Economics of Mental Health Workshop {{ e.year }}" loading="lazy"></a>
</section>
{% endfor %}
