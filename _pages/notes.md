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
    <a href="{{ note.pdf_url }}">[PDF]</a>
  </div>
{% endfor %}
