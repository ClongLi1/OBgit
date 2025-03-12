---
banner: "![[homepage.png]]"
banner_y: 0.886
---

<div style=" width: 50%;  height:30;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/miniTianqi?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&select-theme=ta&theme=%E6%A0%B7%E5%BC%8F4&input-text=&theme-color=%2350F9FFFF&select-icon=durian" allow="fullscreen" style=" height: 200%; width: 200%;"></iframe></div>

![[时间作息表]]


```contributionGraph
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
setting.headerLevel = 3;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = true;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```


