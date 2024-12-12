---
week: 49
month: 12
year: 2024
tags:
  - journal/monthly
---

[[Monthly Review 2024-11|↶ PREVIOUS MONTH]] ⁝ [[Monthly Review 2024-12|THIS MONTH]] ⁝ [[Monthly Review 2025-01|FOLLOWING MONTH ↷]]


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



