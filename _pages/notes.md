---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---

{% for note in site.notes %}
  <div class="note-item">
    <h3>{{ note.title }}</h3>
    <div class="note-description">
      {{ note.content | markdownify }}
    </div>
    <div class="note-pdfs">
      {% if note.pdf_links %}
        {% for pdf in note.pdf_links %}
          <a href="{{ pdf.url }}" class="pdf-link">
            [{{ pdf.name }}]  <!-- 显示自定义名称 -->
          </a>
        {% endfor %}
      {% else %}
        <!-- 兼容旧版单个链接 -->
        <a href="{{ note.pdf_url }}" class="pdf-link">[PDF]</a>
      {% endif %}
    </div>
  </div>
  <hr>
{% endfor %}
