---
title: "Другое"
description: "Справочные материалы"
---

{% assign other = site.pages | where: "category", "other" | sort: "order" %}

{% for o in other %}- [**{{ o.title }}**]({{ o.url | relative_url }}) — {{ o.description }}
{% endfor %}

---

[← На главную]({{ '/' | relative_url }})
