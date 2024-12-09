---
created: 2023-07-09
cssclasses:
  - wide
  - max
tags:
  - dashboard
---
Links:: [[Dashboard]]

---

## Ultimi 30 giorni

```dataview
TABLE

    choice(length(filter(file.tasks, (t) => contains(t.text, "Esercizi") AND t.checked)) > 0, "✅", "❌") AS "💪 Esercizi",

    choice(length(filter(file.tasks, (t) => contains(t.text, "Lettura") AND t.checked)) > 0, "✅", "❌") AS "📚 Lettura"


FROM "2. Areas/Journal/Daily"

// SORT choice(file.name, file.name, "") ASC
SORT choice(!file.name, file.name, file.name) DESC

LIMIT 30
```

## Ultimi 7 giorni

```dataview
TABLE

    choice(length(filter(file.tasks, (t) => contains(t.text, "Esercizi") AND t.checked)) > 0, "✅", "❌") AS "💪 Esercizi",

    choice(length(filter(file.tasks, (t) => contains(t.text, "Lettura") AND t.checked)) > 0, "✅", "❌") AS "📚 Lettura"


FROM "2. Areas/Journal/Daily"

// SORT choice(file.name, file.name, "") ASC
SORT choice(!file.name, file.name, file.name) DESC

LIMIT 7
```










