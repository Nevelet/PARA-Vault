---
limit: 20
mapWithTag: false
icon: goal
tagNames:
  - goal
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
version: "2.107"
fields:
  - name: deadline
    type: Date
    options:
      dateFormat: YYYY-MM-DD
      defaultInsertAsLink: false
    path: ""
    id: YSS1GH
  - name: target
    type: Number
    options: {}
    path: ""
    id: cKItaK
  - name: currently
    type: Number
    options: {}
    path: ""
    id: 8w9KRl
  - name: status
    type: Select
    options:
      valuesList:
        "1": Active
        "2": Pause
        "3": Done
      sourceType: ValuesList
      valuesListNotePath: ""
      valuesFromDVQuery: ""
    path: ""
    id: VSaTaI
  - name: area
    type: MultiFile
    options:
      dvQueryString: dv.pages('#area').where(p => !p.file.path.includes("Templates"))
    path: ""
    id: PDZ2rs
  - name: period
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": Yearly
        "2": Quarterly
        "3": Monthly
        "4": Weekly
    path: ""
    id: 2FIjTx
fieldsOrder:
  - 2FIjTx
  - PDZ2rs
  - VSaTaI
  - 8w9KRl
  - cKItaK
  - YSS1GH
---
