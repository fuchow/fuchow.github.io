---
title: "Discipline Notes"
permalink: /notes/
layout: archive
---

{% for note in site.notes %}
  <div class="publication-item">
    <h3><a href="{{ note.url }}">{{ note.title }}</a></h3>
    <p>{{ note.date | date: "%Y" }} | {{ note.course }}</p>
    <a href="{{ note.pdf_url }}" target="_blank">[PDF]</a>
  </div>
{% endfor %}
