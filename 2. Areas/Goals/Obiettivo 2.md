---
created: 2024-12-10
deadline: 2024-12-31
tags:
  - goal
target: 500
currently: 237
status: Active
area: 
period: Quarterly
---
Links:: [[My Goals]]

---


## Projects

```dataview
TABLE deadline AS Deadline, status AS Status, tags AS Tags

FROM #project  

WHERE 
	contains(goal, this.file.name) OR 
	contains(goal, this.file.link) AND
	!contains(status, "Done")

```



