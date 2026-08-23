---
title: "Таймлайн"
description: "Хронология событий"
---

{% assign timeline = site.pages | where: "category", "timeline" | sort: "order" %}

{% if timeline.size == 0 %}
Раздел пока пуст.

Чтобы добавить материал, положи в папку `timeline/` файл `имя.md`, начинающийся с блока:

    ---
    title: Эра Падения
    description: Короткое пояснение для списка
    category: timeline
    order: 1
    ---

После коммита он сам появится в этом списке, а счётчик на главной обновится.
{% else %}
{% for t in timeline %}- [**{{ t.title }}**]({{ t.url | relative_url }}) — {{ t.description }}
{% endfor %}
{% endif %}

---

[← На главную]({{ '/' | relative_url }})
