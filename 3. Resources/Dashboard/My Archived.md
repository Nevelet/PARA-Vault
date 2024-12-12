---
created: 2023-12-24
tags:
  - dashboard
cssclasses:
  - wide
  - no-wrap
---
Links:: [[_HOME]]

---


## Projects Completed

_Gli ultimi 20 progetti completati_
```dataview
TABLE WITHOUT ID
    file.link as "Projects",
    file.tags as Tags,
    deadline as "Deadline"
    
FROM 
	"4. Archived/Projects Completed" AND #project 

WHERE 
	!contains(file.path, "Templates")
	

// SORT choice(deadline, deadline, "") ASC

SORT choice(!deadline, deadline, deadline) DESC

LIMIT 20
```


