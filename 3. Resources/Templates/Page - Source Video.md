<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Video")
	tR+ await tp.file.move("/3. Resources/Sources/Video/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Sources/Video/" + renameNote)
}

let URL = await tp.system.prompt("URL")

-%>
---
created: <%tp.date.now("YYYY-MM-DD")%>
URL: <%URL%>
author: 
  - <%await tp.system.prompt("Autore")%>
tags:
  - source/video
status: Write
---
Links:: [[My Sources]]

---

![<%renameNote%>](<%URL%>)

<%tp.file.include('[[Heading - Notes]]')%>






<%tp.file.include('[[Heading - Highlights]]')%>

<%tp.file.include('[[Heading - Internal Notes]]')%>

<%tp.file.include('[[Heading - External Links]]')%>

