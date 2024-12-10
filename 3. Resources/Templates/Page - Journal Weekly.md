---
tags:
  - journal/weekly
week: <%tp.date.now("ww", 0, tp.file.title, "YYYY-ww")%>
month: <%tp.date.now("MM", 0, tp.file.title, "YYYY-ww")%>
year: <%tp.date.now("YYYY", 0, tp.file.title, "YYYY-ww")%>
---
[[<%tp.date.now("[Weekly Review] YYYY-[W]ww", -7, tp.file.title, "YYYY-ww")%>|↶ PREVIOUS WEEK]] ⁝ [[<%tp.date.now("[Monthly Review] YYYY-MM", 0, tp.file.title, "YYYY-ww")%>|THIS MONTH]] ⁝ [[<%tp.date.now("[Weekly Review] YYYY-[W]ww", +7, tp.file.title, "YYYY-ww")%>|FOLLOWING WEEK ↷]]

## 🎯 [[My Goals|Obiettivi]]

```dataview
TASK

FROM #journal/monthly  

WHERE 
	contains(month, this.month) AND !completed AND
	contains(meta(section).subpath, "Goals") AND
	!contains(file.path, "Templates")
	

```

Sulla base degli obiettivi mensili, quali sono gli obiettivi che devi raggiungere questa settimana per arrivarci?

- [ ] Obiettivo 1
- [ ] Obiettivo 2
- [ ] Obiettivo 3


## 📅 Agenda

Quali sono gli impegni più importanti di questa settimana?

### **Lunedì**

- [ ] 
- [ ] 
- [ ] 

### **Martedì**

- [ ] 
- [ ] 
- [ ] 

### **Mercoledì**

- [ ] 
- [ ] 
- [ ] 

### **Giovedì**

- [ ] 
- [ ] 
- [ ] 

### **Venerdì**

- [ ] 
- [ ] 
- [ ] 

### **Sabato**

- [ ] 
- [ ] 
- [ ] 

### **Domenica**

- [ ] 
- [ ] 
- [ ] 



## ♻ Habits

| Abitudine   | Lun | Mar | Mer | Gio | Ven | Sab | Dom |     |
| ----------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Esercizio   |     |     |     |     |     |     |     |     |
| Lettura     |     |     |     |     |     |     |     |     |

| Log        | Lun | Mar | Mer | Gio | Ven | Sab | Dom |
| ---------- | --- | --- | --- | --- | --- | --- | --- |
| Mood       |     |     |     |     |     |     |     |
| Energia    |     |     |     |     |     |     |     |
| Ore-Lavoro |     |     |     |     |     |     |     |

## ✅ Checklist

- [ ] Inbox zero
- [ ] Pianificare la settimana prossima


## 🤔 Reflections

  - Quali attività/progetti importante hai completato di ogni particolare area?
	  - 
  - Cosa non sei riuscito a fare e perché?
	  - 
  - Cosa puoi fare per migliorare il prossimo mese?
	  - 

## 🌟 Highlights 

- weekly_log:: 


>[!note]- Daily Log
> ```dataview
> TABLE without id "<br>" + file.link + "<br>" + daily_log as "Daily Log"
> FROM #journal/daily AND "2. Areas/Journal/Daily"
> WHERE contains(file.outlinks, this.file.link) OR contains(week, this.week) AND daily_log != null
> SORT file.day desc
> Limit 7 
> ```

