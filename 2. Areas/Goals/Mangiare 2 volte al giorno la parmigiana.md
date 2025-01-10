---
created: 2024-12-20
deadline: 
tags:
  - goal
target: 2
currently: 1
status: Active
area:
  - "[[; Area 3]]"
period: Weekly
---
Links:: [[My Goals]]

---


## [[My Projects|Projects]]

```dataview
TABLE deadline AS Deadline, status AS Status, tags AS Tags

FROM #project  

WHERE 
	contains(goal, this.file.name) OR 
	contains(goal, this.file.link) AND
	!contains(status, "Done")

```



