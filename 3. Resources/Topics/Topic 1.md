---
tags:
  - topic
cssclasses:
  - wide
  - no-wrap
---
Links:: [[My Topics]]

---

- 


```dataview
TABLE 
	created AS Created
	
FROM [[]] AND !outgoing([[]]) AND !#journal 

WHERE
	!contains(file.path, "Templates")

// SORT choice(created, created, "") ASC
SORT choice(!created, created, created) DESC

LIMIT 30
```


