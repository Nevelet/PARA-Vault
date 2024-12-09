---
created: <%tp.date.now("YYYY-MM-DD")%>
tags:
  - source/movie/serie-tv
status: 
title: 
italianTitle: 
year: 
URL: 
plot: 
genres: 
director: 
duration: 
onlineRating: 
personalRating: 
actors: 
image: 
streamingServices: 
seasonWatch: 
episodeWatch:
---
Links:: [[My Movies]]

---

## 📝 Notes


<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Serie Tv")
	tR+ await tp.file.move("/3. Resources/Movies/Series/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Movies/Series/" + renameNote)
}

-%>

