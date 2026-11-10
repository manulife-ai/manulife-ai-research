---
title: Publications
permalink: /library/publications/
---

# Publications

Peer-reviewed papers and preprints from Manulife AI teams.

{% assign publications = site.library | where: "type", "publication" | sort: "year" | reverse %}
{% assign accepted_publications = publications | where: "status", "accepted" %}
{% assign published_publications = publications | where_exp: "item", "item.status != 'accepted'" %}

{% if accepted_publications.size > 0 %}
## Accepted

<ul class="library-list">
{% for item in accepted_publications %}
{% include library-item.html item=item %}
{% endfor %}
</ul>

## Published

{% endif %}
<ul class="library-list">
{% for item in published_publications %}
{% include library-item.html item=item %}
{% endfor %}
</ul>

{% if publications.size == 0 %}
No publications yet.
{% endif %}
