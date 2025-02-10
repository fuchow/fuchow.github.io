---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---

{% for note in site.notes %}
  <div class="note-item">
    <h3 class="note-title">{{ note.title }}</h3>
    <div class="note-description">
      {{ note.content | markdownify }}  <!-- 显示简介 -->
    </div>
    {% if note.pdf_links %}
      <div class="pdf-links">
        {% for pdf in note.pdf_links %}
          <a href="{{ pdf.url }}" class="pdf-link">{{ pdf.label }}</a>
        {% endfor %}
      </div>
    {% else %}
      <!-- 如果没有 pdf_links，可以回退到单个 pdf_url -->
      <a href="{{ note.pdf_url }}" class="pdf-link">[PDF]</a>
    {% endif %}
  </div>
{% endfor %}

{% endfor %}
