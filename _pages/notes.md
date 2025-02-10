---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---

{% for note in site.notes %}
  <div class="note-item">
    <h3>{{ note.title }}</h3>
    <div class="note-description">
      {{ note.content | markdownify }}  <!-- 显示简介 -->
    </div>
    {% if note.pdf_links %}
      {% for pdf in note.pdf_links %}
        <a href="{{ pdf }}">[PDF]</a>
      {% endfor %}
    {% else %}
      <!-- 如果没有 pdf_links，可以回退到单个 pdf_url -->
      <a href="{{ note.pdf_url }}">[PDF]</a>
    {% endif %}
  </div>
{% endfor %}
