---
limit: 20
mapWithTag: false
icon: file-spreadsheet
tagNames:
  - note
filesPaths: 
bookmarksGroups: 
excludes: 
extends: Standard
savedViews: []
favoriteView: 
fieldsOrder:
  - swTddU
version: "2.17"
fields:
  - name: topics
    type: MultiFile
    options:
      dvQueryString: dv.pages('#topic').where(p => !p.file.path.includes("Templates"))
    path: ""
    id: swTddU
---
