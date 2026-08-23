---
title: "Spacer's Guide to Sol"
description: "Справочник сеттинга для игроков"
---

Человечество расселилось от подземных городов Марса до кочевых караванов Пояса Койпера, и почти всюду успело переругаться. Здесь собрано то, что полезно знать перед вылетом: кто чем владеет, где действуют чьи законы и почему на одних мирах вы дышите свободно, а на других не снимаете маску.

Справочник живой — разделы дополняются по ходу кампании.

{% assign timeline = site.pages | where: "category", "timeline" %}
{% assign factions = site.pages | where: "category", "factions" %}
{% assign other = site.pages | where: "category", "other" %}

<div class="cards">
  <a class="card" href="{{ '/timeline/' | relative_url }}">
    <span class="card-count">{{ timeline | size }}</span>
    <span class="card-name">Таймлайн</span>
    <span class="card-desc">От Эры Падения до наших дней.</span>
    <span class="card-meta">{{ timeline | size }}&nbsp;{% include plural.html n=timeline.size one="материал" few="материала" many="материалов" %}</span>
  </a>
  <a class="card" href="{{ '/factions/' | relative_url }}">
    <span class="card-count">{{ factions | size }}</span>
    <span class="card-name">Фракции</span>
    <span class="card-desc">Государства, кланы и их владения.</span>
    <span class="card-meta">{{ factions | size }}&nbsp;{% include plural.html n=factions.size one="материал" few="материала" many="материалов" %}</span>
  </a>
  <a class="card" href="{{ '/other/' | relative_url }}">
    <span class="card-count">{{ other | size }}</span>
    <span class="card-name">Другое</span>
    <span class="card-desc">Расы, справочные материалы, всё прочее.</span>
    <span class="card-meta">{{ other | size }}&nbsp;{% include plural.html n=other.size one="материал" few="материала" many="материалов" %}</span>
  </a>
</div>
