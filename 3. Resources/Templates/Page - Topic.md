---
tags:
  - topic
cssclasses:
  - wide
  - no-wrap
---
Links:: [[My Topics]]

---

- 


```dataview
TABLE 
	created AS Created
	
FROM [[]] AND !outgoing([[]]) AND !#journal 

WHERE
	!contains(file.path, "Templates")

// SORT choice(created, created, "") ASC
SORT choice(!created, created, created) DESC

LIMIT 30
```


<%* 
let title = tp.file.title
let renameNote

if(title == "Untitled"){
	renameNote = await tp.system.prompt("Nome Topic")
	tR+ await tp.file.move("/3. Resources/Topics/" + title), await tp.file.rename(renameNote)
} else {
	renameNote = tp.file.title.replace("+ ","")
	tR+ await tp.file.move("/3. Resources/Topics/" + renameNote)
}

-%>