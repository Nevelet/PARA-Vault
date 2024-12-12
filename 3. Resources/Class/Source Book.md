---
limit: 20
mapWithTag: false
icon: book
tagNames:
  - source/book
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - ofiG6P
  - CFwOPE
  - HukhM9
  - L2jYyn
  - WuHo5w
  - wihah6
  - ZctlHA
  - sUtjK4
  - lAIgO2
  - Ypjgxt
version: "2.82"
fields:
  - name: title
    type: Input
    options: {}
    path: ""
    id: CFwOPE
  - name: year
    type: Input
    options: {}
    path: ""
    id: L2jYyn
  - name: URL
    type: Input
    options: {}
    path: ""
    id: WuHo5w
  - name: author
    type: Input
    options: {}
    path: ""
    id: HukhM9
  - name: pages
    type: Number
    options: {}
    path: ""
    id: sUtjK4
  - name: pages-read
    type: Number
    options: {}
    path: ""
    id: ZctlHA
  - name: image
    type: Input
    options: {}
    path: ""
    id: lAIgO2
  - name: personalRating
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": ⭐⭐⭐⭐⭐
        "2": ⭐⭐⭐⭐
        "3": ⭐⭐⭐
        "4": ⭐⭐
        "5": ⭐
    path: ""
    id: Ypjgxt
  - name: status
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": Active
        "2": Distill
        "3": Done
    path: ""
    id: ofiG6P
  - name: topics
    type: MultiFile
    options:
      dvQueryString: dv.pages('#topic').where(p => !p.file.path.includes("Templates"))
    path: ""
    id: wihah6
---
