---
title: "Фракции"
description: "Государства, кланы и их владения"
---

{% assign factions = site.pages | where: "category", "factions" | sort: "order" %}
{{ factions | size }} {% include plural.html n=factions.size one="фракция" few="фракции" many="фракций" %}.

{% assign groups = "Солнечная система,Другие системы,Система Стейпл" | split: "," %}
{% for g in groups %}
## {{ g }}

{% for f in factions %}{% if f.group == g %}- [**{{ f.title }}**]({{ f.url | relative_url }}) — {{ f.description }}
{% endif %}{% endfor %}
{% endfor %}

---

[← На главную]({{ '/' | relative_url }})
