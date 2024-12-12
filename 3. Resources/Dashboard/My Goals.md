---
tags:
  - dashboard
cssclasses:
  - no-wrap
  - wide
  - cards
---
Links:: [[Dashboard]]

---
```meta-bind-button
label: Add Goal
icon: goal
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Goals.md
    folderPath: /
    fileName: ""
    openNote: true

```

## Active

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[goal.png|100]]) as Cover,
	file.link AS Goals,
	"Area: " + area AS Area,
	"Target: " + target AS Target,
	"Currently: " + currently AS "currently",
	"Deadline: " + deadline AS Deadline,
	    choice(currently and target, "<progress value='" + string((default(currently, 0) / default(target, 1)) * 100) + "' max='100'></progress>" + " " + round((default(currently, 0) / default(target, 1)) * 100) + "%", "No Data") AS "Progress"

FROM #goal 

WHERE 
	contains(status, "Active") AND 
	!contains(file.path,"Templates") 


```

## Not Active

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[goal.png|100]]) as Cover,
	file.link AS Goals,
	"Area: " + area AS Area,
	"Target: " + target AS Target,
	"Currently: " + currently AS "currently",
	"Deadline: " + deadline AS Deadline,
	    choice(currently and target, "<progress value='" + string((default(currently, 0) / default(target, 1)) * 100) + "' max='100'></progress>" + " " + round((default(currently, 0) / default(target, 1)) * 100) + "%", "No Data") AS "Progress"

FROM #goal 

WHERE 
	contains(status, "Pause") AND 
	!contains(file.path,"Templates") 


```

## Done

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[goal.png|100]]) as Cover,
	file.link AS Goals,
	"Area: " + area AS Area,
	"Target: " + target AS Target,
	"Currently: " + currently AS "currently",
	"Deadline: " + deadline AS Deadline,
	    choice(currently and target, "<progress value='" + string((default(currently, 0) / default(target, 1)) * 100) + "' max='100'></progress>" + " " + round((default(currently, 0) / default(target, 1)) * 100) + "%", "No Data") AS "Progress"

FROM #goal 

WHERE 
	contains(status, "Done") AND 
	!contains(file.path,"Templates") 


```


