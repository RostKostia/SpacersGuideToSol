---
title: "Фракции"
description: "Государства, кланы и их владения"
---

{% assign factions = site.pages | where: "category", "factions" | sort: "order" %}
{{ factions | size }} {% assign n = factions | size %}{% assign m100 = n | modulo: 100 %}{% assign m10 = n | modulo: 10 %}{% if m100 >= 11 and m100 <= 14 %}фракций{% elsif m10 == 1 %}фракция{% elsif m10 >= 2 and m10 <= 4 %}фракции{% else %}фракций{% endif %}.

{% assign groups = "Солнечная система,Другие системы,Система Стейпл" | split: "," %}
{% for g in groups %}
## {{ g }}

{% for f in factions %}{% if f.group == g %}- [**{{ f.title }}**]({{ f.url | relative_url }}) — {{ f.description }}
{% endif %}{% endfor %}
{% endfor %}

---

[← На главную]({{ '/' | relative_url }})
