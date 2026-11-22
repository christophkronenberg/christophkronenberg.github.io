---
layout: default
title: Past workshops
permalink: /workshop/archive/
description: Past editions of the Economics of Mental Health Workshop, 2018 to 2026.
---

<p class="subnav"><a href="{{ '/workshop/' | relative_url }}">&larr; Economics of Mental Health Workshop</a></p>

{% assign editions = site.data.emhw %}
{% for e in editions %}
<section class="edition" id="emhw-{{ e.year }}">
  <h2>{{ e.year }} · {{ e.place }}</h2>
  {% assign flyer_path = '/assets/img/emhw/emhw-' | append: e.year | append: '.jpg' %}
  {% assign thumb_path = '/assets/img/emhw/thumbs/emhw-' | append: e.year | append: '.jpg' %}
  {% assign flyer = site.static_files | where: "path", flyer_path | first %}
  {% assign thumb = site.static_files | where: "path", thumb_path | first %}
  {% if thumb %}{% assign img_path = thumb_path %}{% else %}{% assign img_path = flyer_path %}{% endif %}
  {% if flyer %}<a class="flyer" href="{{ flyer_path | relative_url }}" title="Open the call for papers"><img src="{{ img_path | relative_url }}" alt="Call for papers, Economics of Mental Health Workshop {{ e.year }}" width="480" height="270" loading="lazy"></a>{% endif %}
  {% if e.host %}<p class="meta">Host: {{ e.host }}</p>{% endif %}
  <p><strong>Keynotes:</strong> {{ e.keynotes }}</p>
  {% if e.note %}<p>{{ e.note }}</p>{% endif %}
  {% if e.roundup %}<p><a href="{{ e.roundup }}">Meeting round-up</a></p>{% endif %}
</section>
{% endfor %}
