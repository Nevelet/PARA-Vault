---
created: 2024-03-04
tags:
  - dashboard
area: 
aliases: 
cssclasses:
  - no-wrap
  - wide
---
Links:: [[Dashboard]]

---
## Inbox

- [[Process Inbox]]

## Write

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time

FROM #note

WHERE action = "Write" OR status = "Write"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

FLATTEN tags

LIMIT 30
```

## Distill

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time

FROM #note

WHERE action = "Distill" OR status = "Distill"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

FLATTEN tags

LIMIT 30
```

## Organize

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time

FROM #note

WHERE action = "Organize" OR status = "Organize"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

FLATTEN tags

LIMIT 30
```

- [[No folder]]
- [[No Tags]]
- [[No Inlinks]]


## Express

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time

FROM #note

WHERE action = "Express" OR status = "Express"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

FLATTEN tags

LIMIT 30
```



## 🔗 Internal Links

- [[My Sources]]
- [[Ultime note modificate]]
- [[Ultime note create]]

