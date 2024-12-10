---
created: <%tp.date.now("YYYY-MM-DD")%>
tags:
  - area
aliases: 
cssclasses:
  - wide
  - no-wrap
---
Links:: [[My Areas]]

---


## [[My Goals|Goals]]

```dataview
TABLE deadline AS Deadline
FROM #goal  
WHERE 
	contains(link(Links), link(this.file.name)) OR
	contains(link(area), link(this.file.name)) AND
	contains(status, "Active")

LIMIT 20
```

## [[My Projects|Projects]]

```dataview
TABLE deadline AS Deadline
FROM #project 
WHERE 
	contains(link(Links), link(this.file.name)) OR
	contains(link(area), link(this.file.name)) AND
	contains(status, "Active")

LIMIT 20
```

## [[My Sources|Sources]]

```dataview
TABLE status AS Status
FROM #source 
WHERE 
	contains(link(Links), link(this.file.name)) OR
	contains(link(area), link(this.file.name)) AND
	contains(status, "Active")

LIMIT 20
```

## [[My Notes|Notes]]

```dataview
TABLE status AS Status, created AS Created
FROM #note

WHERE 
	contains(link(Links), link(this.file.name)) OR
	contains(link(area), link(this.file.name)) AND
	contains(status, "Active")

LIMIT 20
```



