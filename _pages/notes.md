---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---
**There exists some mistakes in my notes, please read with caution! All the notes are written by myself, please not priate or disseminate for profits!**

**我的笔记中存在笔误, 请谨慎参考! 所有笔记均由我本人完成, 请不要盗版或以盈利为目的传播!**
<hr>
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
