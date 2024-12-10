---
week: <%tp.date.now("ww", 0, tp.file.title, "YYYY-MM")%>
month: <%tp.date.now("MM", 0, tp.file.title, "YYYY-MM")%>
year: <%tp.date.now("YYYY", 0, tp.file.title, "YYYY-MM")%>
tags:
  - journal/monthly
---

[[<%tp.date.now("[Monthly Review] YYYY-MM", -1, tp.file.title, "YYYY-MM")%>|↶ PREVIOUS MONTH]] ⁝ [[<%tp.date.now("[Monthly Review] YYYY-MM", 0, tp.file.title, "YYYY-MM")%>|THIS MONTH]] ⁝ [[<%tp.date.now("[Monthly Review] YYYY-MM", 31, tp.file.title, "YYYY-MM")%>|FOLLOWING MONTH ↷]]


## 🎯 [[My Goals|Obiettivi]]

```dataview
TASK

FROM #journal/yearly   

WHERE 
	contains(yearly, this.yearly) AND !completed AND
	contains(meta(section).subpath, "Goals") AND
	!contains(file.path, "Templates")
	

```

Sulla base degli obiettivi annuali, quali sono gli obiettivi che devi raggiungere questo mese per arrivarci?

- [ ] Obiettivo 1
- [ ] Obiettivo 2
- [ ] Obiettivo 3



## 🌟 Highlights 

- monthly_log:: 


>[!note]- Weekly Log
> ```dataview
> TABLE without id "<br>" + file.link + "<br>" + weekly_log as "Weekly Log"
> FROM #journal/weekly AND "2. Areas/Journal/Weekly"
> WHERE contains(file.outlinks, this.file.link) OR contains(month, this.month) AND weekly_log != null
> SORT file.day desc
> Limit 7 
> ```

>[!note]- Daily Log
> ```dataview
> TABLE without id "<br>" + file.link + "<br>" + daily_log as "Daily Log"
> FROM #journal/daily AND "2. Areas/Journal/Daily"
> WHERE contains(file.outlinks, this.file.link) OR contains(month, this.month) AND daily_log != null
> SORT file.day desc
> Limit 30 
> ```



