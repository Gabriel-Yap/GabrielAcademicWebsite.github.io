<h2 id="projects" style="margin-top: 40px; margin-bottom: 10px;">Projects</h2>

<div class="projects">
<ol class="bibliography">
{% for link in site.data.projects.main %}
  <li>
    <div class="pub-row">
      <div style="display: flex; align-items: stretch; gap: 24px;">
        {% if link.image %}
        <div style="flex: 0 0 260px; display: flex; align-items: center; justify-content: center;">
          <img src="{{ link.image }}" alt="Project image" style="max-width: 240px; height: auto; border-radius: 14px; box-shadow: 0 2px 8px rgba(0,0,0,0.07); object-fit: contain;">
        </div>
        {% endif %}
        <div style="flex: 1; min-width: 0; display: flex; flex-direction: column; justify-content: center;">
          <div class="title" style="font-weight: bold; font-size: 1.15em; margin-bottom: 0.2em;">{{ link.title }}</div>
          {% if link.date %}
          <div class="project-date" style="color: #888; font-size: 0.95em; margin-bottom: 0.3em;">{{ link.date }}</div>
          {% endif %}
          {% if link.description %}
          <div class="project-description" style="margin-bottom: 0.5em;">{{ link.description }}</div>
          {% endif %}
          {% if link.title contains 'Add2Cart' %}
          <a href="https://add2cart-1755956442426.chatand.build" target="_blank" style="display:inline-block;padding:8px 22px;background:#007bff;color:#fff;border-radius:6px;text-decoration:none;font-weight:500;font-size:1em;margin-bottom:0.5em;box-shadow:0 2px 6px rgba(0,0,0,0.07);">Demo</a>
          {% endif %}
          {% if link.author %}
          <div class="author">{{ link.authors }}</div>
          {% endif %}
          {% if link.periodical or link.conference %}
          <div class="periodical"><em>{{ link.conference }}</em></div>
          {% endif %}
          {% if link.notes %}
          <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
          {% endif %}
          {% if link.others %}
          {{ link.others }}
          {% endif %}
        </div>
      </div>
    </div>
  </li>
  <br>
{% endfor %}
</ol>
</div>
