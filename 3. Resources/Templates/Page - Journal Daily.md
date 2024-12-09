---
week: <%tp.date.now("ww", 0, tp.file.title, "YYYY-MM-DD")%>
quarter: <%tp.date.now("Q", 0, tp.file.title, "YYYY-MM-DD")%>
month: <%tp.date.now("MM", 0, tp.file.title, "YYYY-MM-DD")%>
tags:
  - journal/daily
---
[[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|↶ PREVIOUS DAY]] ⁝ [[<% tp.date.weekday("[Weekly Review] YYYY[-W]WW", 0, tp.file.title, "YYYY-MM-DD") %>|THIS WEEK]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|FOLLOWING DAY ↷]]

# [[<% tp.file.title %>|<% moment(tp.file.title).format("MMMM Do, YYYY") %>]]

> [!quote]
> _“La migliore preparazione per domani è fare il tuo meglio oggi.”_  
> 
> <% tp.web.random_picture("500x500") %>


## 📝 Log

- 

## 🎯 Obiettivi del giorno

```dataview
TASK

FROM #journal/weekly 

WHERE 
	contains(week, this.week) AND !completed AND
	contains(meta(section).subpath, "Goals") AND
	!contains(file.path, "Templates")

```

Sulla base degli obiettivi settimanali, qual è l'unico obiettivo che devi raggiungere oggi per arrivarci?

- [ ] 


## ♻ [[My Habits|Habits]]

- [ ] Esercizi
- [ ] Lettura


## 🌟 Highlights 

- daily_log:: 




## 🤔 Reflection 

**Preoccupazioni del giorno (e come risolverle)**

- 

**Come ti aspetti che vada oggi?**

- 

**3 cose per cui sei grato**

 1. 
 2. 
 3. 

