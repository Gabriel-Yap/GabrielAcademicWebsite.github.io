<h2 id="projects" style="margin-top: 40px; margin-bottom: 10px;">Projects</h2>

<div class="projects">
<ul class="bibliography" style="list-style: none; padding-left: 0;">
{% for link in site.data.projects.main %}
  <li style="margin-bottom: 3.5em;">
    <div class="pub-row">
  <div style="display: flex; align-items: center; gap: 40px;">
        {% if link.image %}
        <div style="flex: 0 0 260px; display: flex; align-items: center; justify-content: center;">
          <img src="{{ link.image }}" alt="Project image" style="max-width: 240px; height: auto; border-radius: 14px; box-shadow: 0 2px 8px rgba(0,0,0,0.07); object-fit: contain;">
        </div>
        {% endif %}
        <div style="flex: 1; min-width: 0; display: flex; flex-direction: column; justify-content: center;">
          <div class="title" style="font-weight: bold; font-size: 1.15em; margin-bottom: 0.2em; display: flex; align-items: center; gap: 10px;">
            <span>{{ link.title }}</span>
            {% if link.title contains 'Add2Cart' %}
              <a href="https://add2cart-1755956442426.chatand.build" target="_blank" title="View Demo" style="display:inline-flex;align-items:center;justify-content:center;width:32px;height:32px;background:#f5f5f5;border-radius:50%;box-shadow:0 2px 6px rgba(0,0,0,0.07);margin-left:2px;text-decoration:none;transition:background 0.2s;">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" viewBox="0 0 24 24"><path fill="#007bff" d="M14 3h7v7h-2V6.41l-9.29 9.3-1.42-1.42L17.59 5H14V3ZM5 5h5V3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2v-5h-2v5H5V5Z"/></svg>
              </a>
            {% endif %}
            {% if link.title contains 'Image Segmentation Project' %}
              <a href="https://github.com/Gabriel-Yap/imagesegmentation" target="_blank" style="display:inline-flex;align-items:center;text-decoration:none;">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="width: 28px; height: 28px; margin-left: 2px; filter: grayscale(0.2);">
              </a>
            {% endif %}
            {% if link.title contains 'Quadtree Image Compression Project' %}
              <a href="https://github.com/Gabriel-Yap/quadtreeimagecompression" target="_blank" style="display:inline-flex;align-items:center;text-decoration:none;">
                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="width: 28px; height: 28px; margin-left: 2px; filter: grayscale(0.2);">
              </a>
            {% endif %}
          </div>
          {% if link.date %}
          <div class="project-date" style="color: #888; font-size: 0.95em; margin-bottom: 0.3em;">{{ link.date }}</div>
          {% endif %}
          {% if link.description %}
          <div class="project-description" style="margin-bottom: 0.5em;">{{ link.description }}</div>
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
  <!-- spacing handled by li margin-bottom -->
{% endfor %}
</ul>
</div>
