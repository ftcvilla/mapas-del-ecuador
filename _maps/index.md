---
layout: home
title: Mapas
permalink: /maps/
---

# Catálogo

<table>
  <thead>
    <tr>
      <th>Título</th>
      <th>Libro de origen</th>
      <th>Autor</th>
      <th>Año</th>
    </tr>
  </thead>

  <tbody>
    {% for map in site.maps %}
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
