---
created: 2023-07-11
tags:
  - dashboard
cssclasses:
  - wide
  - no-wrap
status:
---
Links:: [[My Notes]]

---

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

