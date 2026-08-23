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
    <span class="card-meta">{{ timeline | size }}&nbsp;{% assign n = timeline | size %}{% assign m100 = n | modulo: 100 %}{% assign m10 = n | modulo: 10 %}{% if m100 >= 11 and m100 <= 14 %}материалов{% elsif m10 == 1 %}материал{% elsif m10 >= 2 and m10 <= 4 %}материала{% else %}материалов{% endif %}</span>
  </a>
  <a class="card" href="{{ '/factions/' | relative_url }}">
    <span class="card-count">{{ factions | size }}</span>
    <span class="card-name">Фракции</span>
    <span class="card-desc">Государства, кланы и их владения.</span>
    <span class="card-meta">{{ factions | size }}&nbsp;{% assign n = factions | size %}{% assign m100 = n | modulo: 100 %}{% assign m10 = n | modulo: 10 %}{% if m100 >= 11 and m100 <= 14 %}материалов{% elsif m10 == 1 %}материал{% elsif m10 >= 2 and m10 <= 4 %}материала{% else %}материалов{% endif %}</span>
  </a>
  <a class="card" href="{{ '/other/' | relative_url }}">
    <span class="card-count">{{ other | size }}</span>
    <span class="card-name">Другое</span>
    <span class="card-desc">Расы, справочные материалы, всё прочее.</span>
    <span class="card-meta">{{ other | size }}&nbsp;{% assign n = other | size %}{% assign m100 = n | modulo: 100 %}{% assign m10 = n | modulo: 10 %}{% if m100 >= 11 and m100 <= 14 %}материалов{% elsif m10 == 1 %}материал{% elsif m10 >= 2 and m10 <= 4 %}материала{% else %}материалов{% endif %}</span>
  </a>
</div>
