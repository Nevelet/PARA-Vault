---
limit: 20
mapWithTag: false
icon: file-spreadsheet
tagNames:
  - area-note
filesPaths: 
bookmarksGroups: 
excludes: 
extends: Standard
savedViews: []
favoriteView: 
fieldsOrder:
  - swTddU
version: "2.21"
fields:
  - name: area
    type: MultiFile
    options:
      dvQueryString: dv.pages('#area').where(p => !p.file.path.includes("Templates"))
    path: ""
    id: swTddU
---
