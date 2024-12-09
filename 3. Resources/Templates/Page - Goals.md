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






