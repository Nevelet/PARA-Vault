---
created: <%tp.date.now("YYYY-MM-DD")%>
tags:
  - source/book
status: Active
title: 
year: 
URL: 
author:
  - <%await tp.system.prompt("Autore")%>
pages: <%await tp.system.prompt("Pagine totali")%>
pages-read: 
image: 
onlineRating: 
personalRating: 
topics:
---
Links:: [[My Books]]

---
<%tp.file.include('[[Heading - Notes]]')%>

<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Libro")
	tR+ await tp.file.move("/3. Resources/Sources/Books/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Sources/Books/" + renameNote)
}

-%>



<%tp.file.include('[[Heading - Highlights]]')%>

<%tp.file.include('[[Heading - Internal Notes]]')%>

<%tp.file.include('[[Heading - External Links]]')%>
