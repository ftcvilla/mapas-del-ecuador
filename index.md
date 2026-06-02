---
layout: home
title: Mapas del Ecuador
---

## Catálogo

<table class="catalog">
 <thead>
  <tr>
    <th>Título</th>
    <th>Libro de origen</th>
    <th>Autor del libro</th>
    <th>Año</th>
  </tr>
</thead>

<tbody>
  {% assign sorted_maps = site.maps | sort: "anio" %}

  {% for map in sorted_maps %}
  <tr>
    <td>
      <a href="{{ map.url | relative_url }}">
        {{ map.title }}
      </a>
    </td>

    <td>{{ map.libro_de_origen }}</td>
    <td>{{ map.autor_del_libro }}</td>
    <td>{{ map.anio }}</td>
  </tr>
  {% endfor %}
</tbody>
</table>
