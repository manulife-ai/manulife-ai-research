---
title: Patents
permalink: /library/patents/
---

# Patents

Granted and pending patents from Manulife AI teams.

{% assign patents = site.library | where: "type", "patent" | sort: "year" | reverse %}
<ul class="library-list">
{% for item in patents %}
  <li class="library-item">
    <span class="library-year">{{ item.year }}</span>
    {% if item.external_url %}
    <a href="{{ item.external_url }}" target="_blank" rel="noopener">{{ item.title }}</a>
    {% else %}
    <span class="library-title-pending">{{ item.title }} (coming soon)</span>
    {% endif %}
    {% if item.venue %}<span class="library-venue">{{ item.venue }}</span>{% endif %}
  </li>
{% endfor %}
</ul>

{% if patents.size == 0 %}
No patents yet.
{% endif %}
