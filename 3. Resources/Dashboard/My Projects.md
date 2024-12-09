---
cssclasses:
  - wide
  - no-wrap
tags:
  - dashboard
---
Links:: [[_HOME]]

---

```meta-bind-button
label: Add Project
icon: folder
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Project.md
    folderPath: /
    fileName: ""
    openNote: true

```

## 🟡 Active

```dataview
TABLE WITHOUT ID
    file.link as "Projects",
    file.tags as Tags,
    deadline as "Deadline"
    
FROM #project AND "1. Projects"

WHERE 
	!contains(file.path, "Templates") AND
	!contains(status, "Done") AND
	!contains(status, "Idea")

// SORT choice(deadline, deadline, "") ASC

SORT choice(!deadline, deadline, deadline) DESC


LIMIT 20
```

## 🔴 Not Active

```dataview
TABLE WITHOUT ID
    file.link as "Projects",
    file.tags as Tags,
    deadline as "Deadline"
    
FROM #project 

WHERE 
	contains(file.path, "4. Archived/Projects Future") OR
	contains(file.path, "4. Archived/Projects Waiting") OR
	contains(status, "Waiting") OR
	contains(status, "Pause") AND
	!contains(file.path, "Templates") AND
	!contains(file.path, "4. Archived/Projects Completed")
	

// SORT choice(deadline, deadline, "") ASC

SORT choice(!deadline, deadline, deadline) DESC


LIMIT 20
```


## 🟢 Done

```dataview
TABLE WITHOUT ID
    file.link as "Projects",
    file.tags as Tags,
    deadline as "Deadline"
    
FROM 
	"1. Projects" AND #project 

WHERE 
	!contains(file.path, "Templates") AND
	contains(status, "Done")
	

// SORT choice(deadline, deadline, "") ASC

SORT choice(!deadline, deadline, deadline) DESC


LIMIT 20
```


### Archived

```dataview
TABLE WITHOUT ID
    file.link as "Projects",
    file.tags as Tags,
    deadline as "Deadline"
    
FROM 
	"4. Archived/Projects Completed" AND #project 

WHERE 
	!contains(file.path, "Templates")
	

// SORT choice(deadline, deadline, "") ASC

SORT choice(!deadline, deadline, deadline) DESC


LIMIT 20
```


