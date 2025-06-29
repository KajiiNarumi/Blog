---
layout: home
description: "Blog de tutoriales y recursos prácticos que acompañan al canal de YouTube de Kajii Narumi. Aprende mejor con guías escritas."
---

{% if paginator %}
  <ul>
    {% for post in paginator.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span>{{ post.date | date: "%Y-%m-%d" }}</span>
        {% if post.excerpt %}
          <div>{{ post.excerpt }}</div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>

  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path }}">Entradas más recientes</a>
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path }}">Entradas anteriores</a>
    {% endif %}
  </div>
{% else %}
  <p>No se encontró paginación activa. Revisa tu _config.yml.</p>
{% endif %}
