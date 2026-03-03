---
title: Overview
---

# Manulife AI Research

AI research and applied research are embedded within our business and technology functions. We focus on practical applications that improve outcomes for our customers and operations.

## Latest Updates

{% assign recent_items = site.library | sort: "year" | reverse | limit: 5 %}
<ul class="library-list">
{% for item in recent_items %}
  <li class="library-item">
    <span class="library-year">{{ item.year }}</span>
    <a href="{{ item.external_url }}" target="_blank" rel="noopener">{{ item.title }}</a>
    <span class="library-type">{{ item.type }}</span>
  </li>
{% endfor %}
</ul>

[View all publications →](/library/)

---

## Embedded Domains

AI capabilities are developed within dedicated teams across the organization:

<div class="card-grid">
{% for domain in site.domains %}
  {% assign domain_library_count = site.library | where_exp: "item", "item.domains contains domain.slug" | size %}
  {% assign domain_collab_count = site.data.partnership | where: "domain", domain.slug | size %}
  {% if domain_library_count >= 2 or domain_library_count >= 1 and domain_collab_count >= 1 %}
  <a href="{{ domain.url | relative_url }}" class="card card-link">
    <h3>{{ domain.title }}</h3>
    <p>{{ domain.blurb }}</p>
  </a>
  {% endif %}
{% endfor %}
</div>

[View all domains →](/domains/)

---

## Responsible AI

Our approach to AI is grounded in responsible development and deployment practices:

<div class="announcement-banner">
  <div class="announcement-icon">🛡️</div>
  <div class="announcement-body">
    <strong class="announcement-title">Our Principles</strong>
    <ul class="announcement-list">
      <li><strong>Governance:</strong> All production models undergo review by model risk management</li>
      <li><strong>Three Lines of Defense:</strong> Business units, risk management, and internal audit maintain independent oversight</li>
      <li><strong>Transparency:</strong> We prioritize interpretable models and explainable outputs where feasible</li>
      <li><strong>Fairness:</strong> Bias testing and monitoring are integrated into our model development lifecycle</li>
      <li><strong>Privacy:</strong> Data minimization and privacy-preserving techniques are core design principles</li>
    </ul>
  </div>
</div>

---

## Open Source

We contribute to the broader ML community through open source projects:

<div class="card-grid">
{% for project in site.data.open_source %}
  <div class="card oss-card">
    <h3>
      {% if project.kind == 'dataset' %}🤗 {% endif %}<a href="{{ project.repo_url }}" target="_blank" rel="noopener">{{ project.name }}</a>
      {% if project.kind == 'dataset' %}<span class="oss-kind dataset">dataset</span>{% endif %}
    </h3>
    <span class="oss-status {{ project.status }}">{{ project.status }}</span>
    <p>{{ project.description }}</p>
    <div class="oss-meta">{{ project.team_owner }} · {{ project.license }}</div>
  </div>
{% endfor %}
</div>

[View all projects →](/open-source/)
