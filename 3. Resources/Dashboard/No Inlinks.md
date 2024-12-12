---
cssclasses:
  - wide
---
Links:: [[My Notes]]

---

```dataview
LIST
FROM ""
WHERE length(file.inlinks) = 0 AND !contains(file.path, "Templates") AND !contains(file.path, "Class")
LIMIT 30
SORT created asc
```