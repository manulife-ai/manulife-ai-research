---
title: Library
permalink: /library/
---

# Library

Publications, talks, reports, and patents from AI teams across Manulife.

## Browse by Type

- [Publications]({{ '/library/publications/' | relative_url }}) — peer-reviewed papers and preprints
- [Talks]({{ '/library/talks/' | relative_url }}) — conference presentations and invited talks
- [Partnership]({{ '/partnership/' | relative_url }}) — academic and industry collaborations

---

{% assign accepted_items = site.library | where: "status", "accepted" | sort: "year" | reverse %}
{% if accepted_items.size > 0 %}
## Accepted

<ul class="library-list">
{% for item in accepted_items %}
{% include library-item.html item=item show_type=true %}
{% endfor %}
</ul>
{% endif %}

## All Items

{% assign all_items = site.library | where_exp: "item", "item.status != 'accepted'" | sort: "year" | reverse %}
<ul class="library-list">
{% for item in all_items %}
{% include library-item.html item=item show_type=true %}
{% endfor %}
</ul>
