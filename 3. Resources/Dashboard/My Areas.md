---
tags:
  - dashboard
---




```dataview
LIST 
	
FROM #area  AND !outgoing([[]])

WHERE
	!contains(file.path, "Templates")

// SORT choice(created, created, "") ASC
SORT choice(!created, created, created) DESC

LIMIT 30
```