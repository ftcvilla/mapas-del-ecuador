---
layout: home
title: Mapas del Ecuador
---

# Mapas del Ecuador

Archivo digital de mapas históricos del Ecuador.

## Catálogo

{% for map in site.maps %}
- <a href="/mapas-del-ecuador/maps/{{ map.path | replace: '_maps/', '' | replace: '.md', '' }}/">
  {{ map.title }}
</a> ({{ map.año }})
{% endfor %}
