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
```dataviewjs
let setting = {};

//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";

setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 2;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = true;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```
```dataviewjs
let setting = {};

//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";

setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 2;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = true;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```
```dataviewjs
let setting = {};

//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";

setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 2;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = true;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```


