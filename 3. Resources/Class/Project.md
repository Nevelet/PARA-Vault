---
limit: 20
mapWithTag: false
icon: folder
tagNames:
  - project
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - g1ePul
  - AKqa7C
  - IHwuQT
  - RAZ8iv
  - oSgh0v
version: "2.60"
fields:
  - name: people
    type: MultiFile
    options:
      dvQueryString: dv.pages('#people')
    path: ""
    id: g1ePul
  - name: area
    type: MultiFile
    options:
      dvQueryString: dv.pages('#area')
    path: ""
    id: AKqa7C
  - name: priority
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": High
        "2": Medium
        "3": Low
    path: ""
    id: IHwuQT
  - name: status
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": Idea
        "2": Active
        "3": Waiting
        "4": Pause
        "5": Done
    path: ""
    id: RAZ8iv
  - name: deadline
    type: Date
    options:
      dateShiftInterval: 1 day
      dateFormat: YYYY-MM-DD
      defaultInsertAsLink: false
      linkPath: ""
    path: ""
    id: oSgh0v
---
