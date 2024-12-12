---
created: <%tp.date.now("YYYY-MM-DD")%>
URL: <%await tp.system.prompt("URL")%>
author:
  - <%await tp.system.prompt("Autore")%>
tags:
  - source/article
status: Write
topics: 
note:
---
Links:: [[My Sources]]

---
<%tp.file.include('[[Heading - Notes]]')%>

<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Articolo")
	tR+ await tp.file.move("/3. Resources/Sources/Articles/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Sources/Articles/" + renameNote)
}

-%>


<%tp.file.include('[[Heading - Highlights]]')%>

<%tp.file.include('[[Heading - Internal Notes]]')%>

<%tp.file.include('[[Heading - External Links]]')%>



