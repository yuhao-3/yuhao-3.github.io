## 📝 Publications

<div class="publications">

{% for link in site.data.publications.main %}

<div class="paper-box">
  <div class="paper-box-image">
    {% if link.image %}
    <div style="position: relative;">
      <img src="{{ link.image }}" alt="publication image">
      {% if link.conference_short %}
      <div class="badge">{{ link.conference_short }}</div>
      {% endif %}
    </div>
    {% endif %}
  </div>

  <div class="paper-box-text">
    <div class="title"><a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a></div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank">PDF</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" target="_blank">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" target="_blank">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" target="_blank">BibTex</a>
      {% endif %}
      {% if link.notes %}
      <strong><i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>

{% endfor %}

</div>
