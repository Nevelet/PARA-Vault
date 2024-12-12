---
cssclasses:
  - wide
  - cards
tags:
  - dashboard
---
Links:: [[Dashboard]]

---

```meta-bind-button
label: Add Book
icon: book
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Source Book.md
    folderPath: /
    fileName: ""
    openNote: true

```

## To Read

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[book cover.png|100]]) as Cover,
	file.link AS Books,
	"Pages: " + pages AS Pages,
	"Pages Read: " + pages-read AS "Pages Read",
	"Author: " + author AS Authors,
	"Year: " + year AS Years,
	"Personal Rating: " + personalRating AS "Personal Rating",
	    choice(pages-read and pages, "<progress value='" + string((default(pages-read, 0) / default(pages, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pages-read, 0) / default(pages, 1)) * 100) + "%", "No Data") AS "Progress"

FROM #source/book 

WHERE 
	contains(status, "Active") AND 
	!contains(file.path,"Templates") AND 
	!contains(file.path,"Archived")


```

## To Distill

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[book cover.png|100]]) as Cover,
	file.link AS Books,
	"Pages: " + pages AS Pages,
	"Pages Read: " + pages-read AS "Pages Read",
	"Author: " + author AS Authors,
	"Year: " + year AS Years,
	"Personal Rating: " + personalRating AS "Personal Rating",
	    choice(pages-read and pages, "<progress value='" + string((default(pages-read, 0) / default(pages, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pages-read, 0) / default(pages, 1)) * 100) + "%", "No Data") AS "Progress"

FROM #source/book 

WHERE 
	contains(status, "Distill") AND 
	!contains(file.path,"Templates") AND 
	!contains(file.path,"Archived")


```



## Read

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[book cover.png|100]]) as Cover,
	file.link AS Books,
	"Pages: " + pages AS Pages,
	"Pages Read: " + pages-read AS "Pages Read",
	"Author: " + author AS Authors,
	"Year: " + year AS Years,
	"Personal Rating: " + personalRating AS "Personal Rating",
	    choice(pages-read and pages, "<progress value='" + string((default(pages-read, 0) / default(pages, 1)) * 100) + "' max='100'></progress>" + " " + round((default(pages-read, 0) / default(pages, 1)) * 100) + "%", "No Data") AS "Progress"


FROM #source/book 

WHERE contains(status, "Done")

```

