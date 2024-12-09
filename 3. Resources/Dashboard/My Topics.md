---
tags:
  - dashboard
---
Links:: [[Dashboard]]

---

```dataview
LIST
FROM #topic AND !outgoing([[]])
WHERE !contains(file.path, "Templates")
```


