---
created: <%tp.date.now("YYYY-MM-DD")%>
deadline: 
tags:
  - project
status: 
priority: 
area:
---
Links:: [[My Projects]]

---
<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Progetto")
	tR+ await tp.file.move("/1. Projects/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("pj ","")
	tR+ await tp.file.move("/1. Projects/" + renameNote)
}

-%>
# 📝 Notes




# 🧠 Brainstorm

- 


## ✅ TODO

- [ ] 


