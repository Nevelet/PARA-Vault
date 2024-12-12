---
limit: 20
mapWithTag: false
icon: newspaper
tagNames: 
filesPaths: 
bookmarksGroups: 
excludes: 
extends: Standard
savedViews: []
favoriteView: 
version: "2.44"
fields:
  - name: URL
    type: Input
    options: {}
    path: ""
    id: YhC2VL
  - name: status
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": Write
        "2": Distill
        "3": Organize
        "4": Express
        "5": Done
    path: ""
    id: 2FkxDI
  - name: note
    type: Input
    options: {}
    path: ""
    id: ar3McP
  - name: author
    type: Input
    options: {}
    path: ""
    id: go7hDK
  - name: topics
    type: MultiFile
    options:
      dvQueryString: dv.pages('#topic').where(p => !p.file.path.includes("Templates"))
    path: ""
    id: wEaQlK
fieldsOrder:
  - ar3McP
  - 2FkxDI
  - go7hDK
  - wEaQlK
  - YhC2VL
---
