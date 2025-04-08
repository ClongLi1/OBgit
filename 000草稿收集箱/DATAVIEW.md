---
tags: []
date: "\n"
---
```dataview
table tags 
where file = this.file 
```
```dataviewjs
dv.list(dv.pages("").file.tags.distinct())
```
