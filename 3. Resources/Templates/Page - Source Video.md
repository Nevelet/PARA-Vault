---
created: <%tp.date.now("YYYY-MM-DD")%>
URL: 
author: 
tags:
  - source/video
status: Write
area:
---
Links:: [[My Sources]]

---
<%tp.file.include('[[Heading - Notes]]')%>

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

-%>


<%tp.file.include('[[Heading - Highlights]]')%>

<%tp.file.include('[[Heading - Internal Notes]]')%>

<%tp.file.include('[[Heading - External Links]]')%>

