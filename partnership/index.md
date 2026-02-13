---
title: Partnership
permalink: /partnership/
---

# Partnership

We partner with leading academic institutions and industry organizations to advance AI research relevant to insurance and financial services.

{% assign current_partnerships = site.data.partnership | where: "status", "current" %}
{% assign past_partnerships = site.data.partnership | where: "status", "past" %}

{% if current_partnerships.size > 0 %}
## Current Partnerships

<ul class="collab-list">
{% for collab in current_partnerships %}
  <li class="collab-item">
    <strong>{{ collab.partner }}</strong>
    <span class="collab-type">{{ collab.type }}</span>
    <span class="collab-years">{{ collab.years }}</span>
    <p>{{ collab.area }}</p>
    {% if collab.links %}
    <ul class="collab-links">
      {% for link in collab.links %}
      <li><a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a></li>
      {% endfor %}
    </ul>
    {% endif %}
    {% assign domain = site.domains | where: "slug", collab.domain | first %}
    {% if domain %}
    <div class="oss-meta">Related domain: <a href="{{ domain.url | relative_url }}">{{ domain.title }}</a></div>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}

{% if past_partnerships.size > 0 %}
## Past Partnerships

<ul class="collab-list">
{% for collab in past_partnerships %}
  <li class="collab-item">
    <strong>{{ collab.partner }}</strong>
    <span class="collab-type">{{ collab.type }}</span>
    <span class="collab-years">{{ collab.years }}</span>
    <p>{{ collab.area }}</p>
    {% if collab.links %}
    <ul class="collab-links">
      {% for link in collab.links %}
      <li><a href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a></li>
      {% endfor %}
    </ul>
    {% endif %}
    {% assign domain = site.domains | where: "slug", collab.domain | first %}
    {% if domain %}
    <div class="oss-meta">Related domain: <a href="{{ domain.url | relative_url }}">{{ domain.title }}</a></div>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}