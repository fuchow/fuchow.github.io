---
title: "Teaching Assistant"
permalink: /ta/
layout: archive
---

<div class="ta-list">
  {% for item in site.ta %}
    <div class="ta-item">
      <h3>{{ item.title }}</h3>
      <div class="ta-description">
        {{ item.content | markdownify }}
      </div>
      <div class="ta-pdfs">
        {% for pdf in item.pdfs %}
          <a href="{{ pdf.url }}" target="_blank">[{{ pdf.name }}]</a>
        {% endfor %}
      </div>
    </div>
    <hr>
  {% endfor %}
</div>
