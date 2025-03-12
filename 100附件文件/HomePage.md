---
banner: "![[homepage.png]]"
banner_y: 0.886
---

--- start-multi-column: ID_luwl
```column-settings
Number of Columns: 2
Largest Column: standard
```
--- column-break ---

```button
name pkmer
type link
action https://pkmer.cn/
color blue
```
^button-PKMer

--- column-break ---

```button
name 程序员盒子
type link
action https://www.coderutil.com/
color green
```
^button-Coder

--- end-multi-column




<div style=" width: 50%;  height:30;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/miniTianqi?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&select-theme=ta&theme=%E6%A0%B7%E5%BC%8F4&input-text=&theme-color=%2350F9FFFF&select-icon=durian" allow="fullscreen" style=" height: 200%; width: 200%;"></iframe></div>

  ![[OB.jpg|OL|220x300]]✨ **欢迎来到我的黑曜石Obsidian知识库！** 🌟
这里是我的个人数字花园，更是我精心打造的知识宝库。在这个库里，你可以发现各种各样的笔记，从工作中的项目规划、行业动态分析，到个人成长中的读书心得、技能学习总结，应有尽有。 🌱
我将每一个灵感瞬间、每一次深入思考都记录在此，并通过黑曜石强大的双向链接功能，让这些知识相互交织，形成独一无二的知识网络。 💡这个库不仅帮助我高效整理思绪、回顾过往经验，还能助力我快速找到解决问题的灵感。它见证了我一路以来的成长与进步，相信也会成为你探索知识、激发创意的好帮手。 🚀快来一起探索吧！✨
  ```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = " 您已使用 **Obsidian** `"+total+"` 天，"
let nofold = '!"misc/templates"'
let allFile = dv.pages(nofold).file
let totalMd = "共创建 `"+
	allFile.length+"` 篇笔记"
let totalTag = allFile.etags.distinct().length+" 个标签"

dv.paragraph(
	totalDays+totalMd+"、"+totalTag+""
)
``` 


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



