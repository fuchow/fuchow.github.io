---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---

<div class="notes-list">
  {% for note in site.notes %}
    <div class="note-item">
      <h3 class="note-title">{{ note.title }}</h3>
      <div class="note-description">
        {{ note.content | markdownify }}  <!-- 显示简介内容 -->
      </div>
      <a class="note-pdf-link" href="{{ note.pdf_url }}" target="_blank">[PDF]</a>
    </div>
    <hr>
  {% endfor %}
</div>
