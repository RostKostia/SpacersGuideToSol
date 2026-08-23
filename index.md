---
title: "Spacer's Guide to Sol"
description: "Справочник сеттинга для игроков"
---

Человечество расселилось от подземных городов Марса до кочевых караванов Пояса Койпера, и почти всюду успело переругаться. Здесь собрано то, что полезно знать перед вылетом: кто чем владеет, где действуют чьи законы и почему на одних мирах вы дышите свободно, а на других не снимаете маску.

Справочник живой — разделы дополняются по ходу кампании.

{% assign timeline = site.pages | where: "category", "timeline" %}
{% assign factions = site.pages | where: "category", "factions" %}
{% assign other = site.pages | where: "category", "other" %}

## Разделы

### [Таймлайн]({{ '/timeline/' | relative_url }})
{{ timeline | size }} {% include plural.html n=timeline.size one="материал" few="материала" many="материалов" %} — от Эры Падения до наших дней.

### [Фракции]({{ '/factions/' | relative_url }})
{{ factions | size }} {% include plural.html n=factions.size one="материал" few="материала" many="материалов" %} — государства, кланы и их владения.

### [Другое]({{ '/other/' | relative_url }})
{{ other | size }} {% include plural.html n=other.size one="материал" few="материала" many="материалов" %} — расы, справочные материалы, всё прочее.
