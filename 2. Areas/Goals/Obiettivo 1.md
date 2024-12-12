---
created: 2024-12-10
deadline: 
tags:
  - goal
target: 10
currently: 5
status: Active
area:
  - "[[; Area 1]]"
period: Yearly
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




