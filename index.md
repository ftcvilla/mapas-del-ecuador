---
layout: home
title: Mapas
---

## Catálogo

<input
  type="text"
  id="mapSearch"
  placeholder="Buscar mapas..."
  style="width: 100%; padding: 8px; margin-bottom: 12px;">

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
function initMapSearch() {
  const input = document.getElementById("mapSearch");
  if (!input) return;

  const rows = document.querySelectorAll(".catalog tbody tr");

  input.addEventListener("input", function () {
    const value = this.value.toLowerCase();

    rows.forEach(row => {
      const text = row.textContent.toLowerCase();
      row.style.display = text.includes(value) ? "" : "none";
    });
  });
}

if (document.readyState === "loading") {
  document.addEventListener("DOMContentLoaded", initMapSearch);
} else {
  initMapSearch();
}
</script>
