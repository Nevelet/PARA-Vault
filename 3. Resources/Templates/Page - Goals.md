---
created: <%tp.date.now("YYYY-MM-DD")%>
deadline: 
tags:
  - goal
target: 
currently: 
status: 
area: 
period:
---
Links:: [[My Goals]]

---
<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Obiettivo")
	tR+ await tp.file.move("/2. Areas/Goals/" + title), await tp.file.rename(renameNote)
} else {
	tR+ await tp.file.move("/2. Areas/Goals/" + renameNote)
}

-%>


## [[My Projects|Projects]]

```dataview
TABLE deadline AS Deadline, status AS Status, tags AS Tags

FROM #project  

WHERE 
	contains(goal, this.file.name) OR 
	contains(goal, this.file.link) AND
	!contains(status, "Done")

```



