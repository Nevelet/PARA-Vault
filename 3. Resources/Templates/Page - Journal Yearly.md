---
year: <%tp.date.now("YYYY", 0, tp.file.title, "YYYY")%>
tags:
  - journal/yearly
---

[[<%tp.date.now("[Yearly Review] YYYY", "P-1Y", tp.file.title, "YYYY")%>|↶ PREVIOUS YEAR]] ⁝ [[Monthly Review <%tp.date.now("YYYY-MM") %>|THIS MONTH]] ⁝ [[<%tp.date.now("[Monthly Review] YYYY", "P1Y", tp.file.title, "YYYY")%>|FOLLOWING YEAR ↷]]


## 🎯 Goals

Sulla base di questi [[My Goals|obiettivi]], quali sono gli obiettivi che devi raggiungere quest'anno per arrivarci?

- [ ] Obiettivo 1
- [ ] Obiettivo 2
- [ ] Obiettivo 3



## 🌟 Highlights 

- 


>[!note]- Monthly Log
> ```dataview
> TABLE without id "<br>" + file.link + "<br>" + monthly_log as "Weekly Log"
> FROM #journal/monthly AND "2. Areas/Journal/Monthly"
> WHERE contains(file.outlinks, this.file.link) OR contains(year, this.year) AND monthly_log != null
> SORT file.day desc
> Limit 7 
> ```