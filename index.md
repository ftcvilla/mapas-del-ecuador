---
layout: home
title: Mapas del Ecuador
---

# Mapas del Ecuador

Archivo digital de mapas históricos del Ecuador.

## Catálogo

{% for map in site.maps %}
- <a href="{{ map.url }}">{{ map.title }}</a> ({{ map.año }})
{% endfor %}
