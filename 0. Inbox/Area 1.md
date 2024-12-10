---
created: 2024-12-10
tags:
  - area
aliases: 
cssclasses:
  - wide
  - no-wrap
---
Links:: [[My Areas]]

---



## Goals

```dataview
TABLE deadline AS Deadline
FROM #goal  
WHERE 
	contains(Links, this.file.link) AND
	contains(status, "Active")

LIMIT 20
```

## Projects

```dataview
TABLE deadline AS Deadline
FROM #project 
WHERE 
	contains(Links, this.file.link) AND
	contains(status, "Active")

LIMIT 20
```

## Sources

```dataview
TABLE status AS Status
FROM #source 
WHERE 
	contains(Links, this.file.link) AND
	!contains(status, "Done")

LIMIT 20
```

## Notes

```dataview
TABLE status AS Status, created AS Created
FROM #note 
WHERE contains(Links, this.file.link)

LIMIT 20
```



