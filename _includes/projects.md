<h2 id="projects" style="margin-top: 40px; margin-bottom: 10px;">Projects</h2>

<div class="projects">
<ol class="bibliography">
{% for link in site.data.projects.main %}
  <li>
    <div class="pub-row">
      {% if link.image %}
      <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
        <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="max-width:100%;height:auto;">
        {% if link.conference_short %}
        <abbr class="badge">{{ link.conference_short }}</abbr>
        {% endif %}
      </div>
      {% endif %}
      <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
        <div class="title">{{ link.title }}</div>
        <div class="author">{{ link.authors }}</div>
        <div class="periodical"><em>{{ link.conference }}</em></div>
        {% if link.notes %}
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %}
        {{ link.others }}
        {% endif %}
      </div>
    </div>
  </li>
  <br>
{% endfor %}
</ol>
</div>
