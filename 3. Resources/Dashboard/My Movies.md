---
cssclasses:
  - wide
  - cards
tags:
  - dashboard
---
Links:: [[Dashboard]]

---

## Film

```meta-bind-button
label: Add Film
icon: film
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Source Movie (Film).md
    folderPath: /
    fileName: ""
    openNote: true

```

```dataview
TABLE  WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[no cover image.png|100]]) as Cover,
	file.link AS Film, year AS Year, genres AS Genre, 
	"Status: " + status AS Status,
	"Titolo Italiano: " + italianTitle AS "Titolo Italiano",
	"Online Rating: " + onlineRating AS "Online Rating", 
	"Personal Rating: " + personalRating AS "Personal Rating", 
	streamingServices AS "Streaming Services",
	elink(trailer, "Trailer") AS "Trailer",
	"Streaming: " + streaming AS "Streaming"

FROM #source/movie/film 

WHERE !contains(file.path, "Templates")

SORT genres ASC
SORT status ASC
```

## Serie Tv

```meta-bind-button
label: Add Serie Tv
icon: film
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: templaterCreateNote
    templateFile: 3. Resources/Templates/Page - Source Movie (Serie Tv).md
    folderPath: /
    fileName: ""
    openNote: true

```

```dataview
TABLE WITHOUT ID 
	choice(image, ("![coverimg|100](" + image + ")"), ![[no cover image.png|100]]) as Cover, 
	file.link AS Film, year AS Year, genres AS Genre, 
	"Status: " + status AS Status,
	"Online Rating: " + onlineRating AS "Online Rating", 
	"Personal Rating: " + personalRating AS "Personal Rating",  
	"Season to Watch: " + seasonWatch AS "Season to Watch",
	"Episode to Watch: " + episodeWatch AS "Episode to Watch",
	"Platoform: " + streamingServices AS "Streaming Services"

FROM #source/movie/serie-tv 

WHERE !contains(file.path, "Templates")

SORT genres ASC
SORT status ASC
```

