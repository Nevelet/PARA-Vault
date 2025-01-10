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
**Se vuoi saperne di più in merito a come imposto gli obiettivi su Obsidian, puoi guardare [questo video](https://youtu.be/Z2QrTltxWZg?si=rmsrp_C5sAfM-8QU)**

## ❓ Domande e risposte

**Perché vuoi raggiungere questo obiettivo?**

- 
- 
- 

**Che persona devi essere per raggiungere questo obiettivo?**

- 
- 
- 

**Cosa ti spinge a farlo?**

- 
- 
- 

**Che regole devi seguire per raggiungere questo obiettivo?**

- 
- 
- 

**Quali sono i problemi che potresti riscontare?**

- 
- 
- 

**Quali sono le cause che portano ai problemi?**

- 
- 
- 

## 🎬 Piano d'azione

- 
- 
- 

### [[My Projects|Projects]]

```dataview
TABLE deadline AS Deadline, status AS Status, tags AS Tags

FROM #project  

WHERE 
	contains(goal, this.file.name) OR 
	contains(goal, this.file.link) AND
	!contains(status, "Done")

```



## 📉 Monitoraggio

- 
- 
- 

