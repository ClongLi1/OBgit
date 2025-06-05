---
tags:
  - "#标签"
  - 词云
date:
---
```dataview
table tags 
where file = this.file 
```
```dataviewjs
dv.list(dv.pages("").file.tags.distinct())
```
