---
banner: "![[homepage.png]]"
banner_y: 0.886
---



![[时间作息表]]

---

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

---

```dataviewjs
let setting = {};

//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";

setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 3;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = true;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```


