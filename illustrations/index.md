---
layout: home
title: Ilustraciones
permalink: /illustrations/
---

# Ilustraciones

<div class="illustrations-grid">

  {% for ill in site.illustrations %}

  <div class="illustration-item">

    <a href="{{ ill.url | relative_url }}">
      <img src="{{ ill.image | relative_url }}" alt="{{ ill.title }}">
    </a>

    <h3>
      <a href="{{ ill.url | relative_url }}">
        {{ ill.title }}
      </a>
    </h3>

    <p>{{ ill.libro_de_origen }}</p>

    {% if ill.anio %}
    <p>{{ ill.anio }}</p>
    {% endif %}

  </div>

  {% endfor %}

</div>

  </div>

  {% endfor %}

</div>
