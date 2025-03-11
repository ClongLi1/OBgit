---
banner: "![[homepage.png]]"
banner_y: 0.886
sticker: emoji//1f305
---
```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = " 您已使用 `Obsidian` "+total+" 天，"
let nofold = '!"misc/templates"'
let allFile = dv.pages(nofold).file
let totalMd = "共创建 "+
	allFile.length+" 篇📆笔记"
let totalTag = allFile.etags.distinct().length+" 个🧰标签"

dv.paragraph(
	totalDays+totalMd+"、"+totalTag+""
)
```
![[时间作息表]]
```contributionGraph
title: 🏳️‍🌈Obsidian热力图🔥
graphType: default
dateRangeValue: 700
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
cellStyleRules: []

```





