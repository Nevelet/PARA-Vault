---
created: <%tp.date.now("YYYY-MM-DD")%>
aliases:
  - 
tags: people
---
<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Persona")
	tR+ await tp.file.move("/3. Resources/People/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("@ ","")
	tR+ await tp.file.move("/3. Resources/People/" + renameNote)
}

-%>
## ℹ️ About

-

## ⏰ Reminders

- 

## 📝 Notes

- 

---

