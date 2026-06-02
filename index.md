---
layout: home
title: Mapas del Ecuador
---

## Catálogo

<input
  type="text"
  id="mapSearch"
  placeholder="Buscar mapas..."
  style="width: 100%; padding: 8px; margin-bottom: 12px;"
>

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

<script>
window.addEventListener("DOMContentLoaded", function () {
  const input = document.getElementById("mapSearch");

  input.addEventListener("keyup", function () {
    const value = this.value.toLowerCase();
    const rows = document.querySelectorAll(".catalog tbody tr");

    rows.forEach(row => {
      const text = row.innerText.toLowerCase();
      row.style.display = text.includes(value) ? "" : "none";
    });
  });
});
</script>
