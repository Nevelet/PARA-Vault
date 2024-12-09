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
version: "2.103"
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
  - name: goal-outcome
    type: MultiFile
    options:
      dvQueryString: dv.pages('#goal/outcome')
    path: ""
    id: RLNeoO
  - name: goal-value
    type: MultiFile
    options:
      dvQueryString: dv.pages('#goal/value')
    path: ""
    id: yqkTHN
  - name: area
    type: MultiFile
    options:
      dvQueryString: dv.pages('#area')
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
  - yqkTHN
  - RLNeoO
  - VSaTaI
  - 8w9KRl
  - cKItaK
  - YSS1GH
---
