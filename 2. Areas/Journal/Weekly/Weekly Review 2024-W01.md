---
tags:
  - journal/weekly
week: 01
month: 01
year: 2024
---
[[Weekly Review 2023-W52|↶ PREVIOUS WEEK]] ⁝ [[Monthly Review 2024-01|THIS MONTH]] ⁝ [[Weekly Review 2024-W02|FOLLOWING WEEK ↷]]

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

| Abitudine        | Lun | Mar | Mer | Gio | Ven | Sab | Dom |     |
| ---------------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Esercizio        | ✅   |     |     | ✅   |     |     |     |     |
| Lettura          |     | ✅   |     |     | ✅   |     |     |     |
| Meditazione      |     | ✅   |     |     |     |     |     |     |
| Creare contenuti |     |     |     |     |     |     |     |     |

**Fisico**
- Esercizio fisico (2/5)

**Mente**
- Lettura (0/5)
- Meditazione (0/5)

**Business**
- Creare contenuti (0/5)


## ⌚ Log

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

