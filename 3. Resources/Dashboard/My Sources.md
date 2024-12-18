---
tags:
  - dashboard
cssclasses:
  - wide
  - no-wrap
---
Links:: [[My Notes]]

---
_Le note vengono gestite seguendo [[Status Notes|questi stati]]_


```meta-bind-button
label: Add Source
icon: newspaper
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Templater - Select Type Source.md
    folderPath: /
    fileName: ""
    openNote: true

```

## Captured

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time, 
	string(author) AS Author, 
	URL

FROM #source

WHERE 
	action = "Captured" OR 
	status = "Captured" AND 
	!contains(file.path, "Templates") 

SORT choice(!created, created, created) DESC

LIMIT 10 
```


## Write

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time, 
	string(author) AS Author, 
	URL

FROM #source

WHERE 
	action = "Write" OR 
	status = "Write" AND 
	!contains(file.path, "Templates") 

SORT choice(!created, created, created) DESC

LIMIT 10 
```


## Distill

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time, 
	string(author) AS Author, 
	URL

FROM #source

WHERE 
	action = "Distill" OR 
	status = "Distill" AND 
	!contains(file.path, "Templates") 

SORT choice(!created, created, created) DESC

LIMIT 20
```

## Organize

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time, 
	string(author) AS Author, 
	URL

FROM #source

WHERE 
	action = "Organize" OR 
	status = "Organize" AND 
	!contains(file.path, "Templates") 

SORT choice(!created, created, created) DESC

LIMIT 20
```

## Done

```dataview
TABLE 
	note AS Note, 
	dateformat(created, "yyyy-MM-dd") AS Created, 
	date(today) -created AS Time, 
	string(author) AS Author, 
	URL

FROM #source

WHERE 
	action = "Done" OR 
	status = "Done" AND 
	!contains(file.path, "Templates") 

SORT choice(!created, created, created) DESC

LIMIT 10 
```


