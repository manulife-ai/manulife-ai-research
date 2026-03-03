---
title: Open Source
permalink: /open-source/
---

# Open Source

We contribute to the broader machine learning community through open source projects.

<div class="announcement-banner">
  <div class="announcement-icon">🐍</div>
  <div class="announcement-body">
    <strong class="announcement-title">Proud sponsor of the Python Software Foundation</strong>
    <p class="announcement-text">We're excited to give back to the community that powers so much of our work. Come find us at <a href="https://us.pycon.org/2026/" target="_blank" rel="noopener">PyCon US 2026</a> — May 14–22, 2026 in Long Beach, California.</p>
  </div>
</div>

<div class="card-grid">
{% for project in site.data.open_source %}
  <div class="card oss-card">
    <h3>
      {% if project.kind == 'dataset' %}🤗 {% endif %}<a href="{{ project.repo_url }}" target="_blank" rel="noopener">{{ project.name }}</a>
      {% if project.kind == 'dataset' %}<span class="oss-kind dataset">dataset</span>{% endif %}
    </h3>
    <span class="oss-status {{ project.status }}">{{ project.status }}</span>
    <p>{{ project.description }}</p>
    <div class="oss-meta">
      <strong>Team:</strong> {{ project.team_owner }}<br>
      <strong>License:</strong> {{ project.license }}<br>
      <strong>Last Release:</strong> {{ project.last_release }}
    </div>
  </div>
{% endfor %}
</div>
