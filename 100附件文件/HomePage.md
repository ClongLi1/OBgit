---
banner: "![[homepage.png]]"
banner_y: 0.886
banner_x: "0.0001"
---
```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = " 您已使用 `Obsidian` "+total+" 天，"
let nofold = '!"misc/templates"'
let allFile = dv.pages(nofold).file
let totalMd = "共创建 "+
	allFile.length+" 篇笔记"
let totalTag = allFile.etags.distinct().length+" 个标签"

dv.paragraph(
	totalDays+totalMd+"、"+totalTag+""
)
```


--- start-multi-column: ID_8kc5
```column-settings
Number of Columns: 2
Largest Column: standard
```

```contributionGraph
title: Contributions
graphType: default
dateRangeValue: 180
dateRangeType: LATEST_DAYS
startOfWeek: 1
showCellRuleIndicators: true
titleStyle:
  textAlign: left
  fontSize: 15px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField: {}
fillTheScreen: false
enableMainContainerShadow: false
cellStyleRules:
  - id: Lovely_a
    color: "#fedcdc"
    min: 1
    max: 2
  - id: Lovely_b
    color: "#fdb8bf"
    min: 2
    max: 3
  - id: Lovely_c
    color: "#f892a9"
    min: 3
    max: 5
  - id: Lovely_d
    color: "#ec6a97"
    min: 5
    max: 9999

```


--- column-break ---

```tagcloud

```

--- end-multi-column

