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
_Le note vengono gestite seguendo [[Status Notes|questi stati]]_


```meta-bind-button
label: Add Note
icon: notepad-text
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Note General.md
    folderPath: /
    fileName: ""
    openNote: true

```

## Inbox

```dataview
TABLE 
	status AS Status, 
	note AS Note, 
	tags AS Tags, 
	created AS Created, 
	date(today) -created AS Time, 
	Links
	
FROM "0. Inbox"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

LIMIT 20
```

## Write

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time

FROM #note

WHERE status = "Write"

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

WHERE status = "Distill"

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

WHERE status = "Organize"

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

WHERE status = "Express"

SORT choice(created, created, "") ASC
// SORT choice(!created, created, created) DESC

FLATTEN tags

LIMIT 30
```



## 🔗 Internal Links

- [[My Sources]]
- [[Ultime note modificate]]
- [[Ultime note create]]

