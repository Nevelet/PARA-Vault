---
cssclasses:
  - max
  - wide
---
Links:: [[My Notes]]

---


```dataview
TABLE created AS Created, length(file.inlinks) AS Inlinks
FROM "" 
WHERE file.tags AND file.name != this.file.name 
LIMIT 20
```