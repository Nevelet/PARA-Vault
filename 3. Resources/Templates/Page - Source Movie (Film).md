---
created: <%tp.date.now("YYYY-MM-DD")%>
tags:
  - source/movie/film
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
actors: 
image: 
streamingServices: 
personalRating:
---
Links:: [[My Movies]]

---

<%tp.file.include('[[Heading - Notes]]')%>


<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Film")
	tR+ await tp.file.move("/3. Resources/Movies/Film/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Movies/Film/" + renameNote)
}

-%>


