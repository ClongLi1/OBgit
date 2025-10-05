<div style=" width: 100%; height:250;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/Carousel?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe></div>   

```contributionGraph
title: ""
graphType: default
dateRangeValue: 400
dateRangeType: LATEST_DAYS
startOfWeek: 1
showCellRuleIndicators: true
titleStyle:
  textAlign: center
  fontSize: 15px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField: {}
fillTheScreen: false
enableMainContainerShadow: false
cellStyleRules:
  - id: Halloween_a
    color: "#fdd577"
    min: 1
    max: 2
  - id: Halloween_b
    color: "#faaa53"
    min: 2
    max: 3
  - id: Halloween_c
    color: "#f07c44"
    min: 3
    max: 5
  - id: Halloween_d
    color: "#d94e49"
    min: 5
    max: 9999
mainContainerStyle:
  backgroundColor: "#00000007"

```
```dataviewjs  
let ftMd = dv.pages("").file.sort(t => t.cday)[0];  
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));  
let rainbowStyle = "color: #FFFFFF; background: linear-gradient(90deg, #4169E1, #00BFFF, #32CD32, #FFD700, #FF6347, #9932CC); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: bold;";  
let totalDays = `<span style="${rainbowStyle}"> 我在 Obsidian中已探索 ${total} 天 ，</span>`;  
let nofold = '!"misc/templates"';  
let allFile = dv.pages(nofold).file;  
let totalMd = `<span style="${rainbowStyle}">已发现 ${allFile.length} 颗闪耀的笔记星星 </span>`;  
let tagDescription = `<span style="${rainbowStyle}">它们被分类在 ${allFile.etags.distinct().length} 个标签中 </span>`;  
let totalTag = `<span style="${rainbowStyle}">，${tagDescription}</span>`;  
let taskDescription = `<span style="${rainbowStyle}">还有 ${allFile.tasks.length} 个任务等待我去完成，它们如同纽带连接着不同的知识领域 </span>`;
let totalTask = `<span style="${rainbowStyle}">，${taskDescription}</span>`;  

dv.paragraph(totalDays + " " + totalMd + " " + totalTag + " " + totalTask);  
```
![[🌈炫彩时间轴🌈（时间流逝🫧在这一刻被具象化💥）]]
<div style="display: flex; flex-wrap: wrap; justify-content: space-between;">  
  <!-- 左侧栏 -->
    <div style="width: 48%; margin-bottom: 1px;">  
    <!-- Obsidian logo 和欢迎语 -->
    <div style="display: flex; align-items: center; margin-bottom: 1px;">
      <img src="https://fig-1321973591.cos.ap-nanjing.myqcloud.com/Pasted%20image%2020250907225739.png" alt="Obsidian Logo" style="width: 250px; height: 320px; margin-right: 20px;">
      <div>
        <h4>✨ 欢迎来到 Obsidian 知识库🌟</h4>
        <p>🔥这是我的个人数字花园，更是我精心打造的知识宝库。在这里，你可以发现各种各样的笔记，💗从工作中的项目规划、行业动态分析，到个人成长中的读书心得、技能学习总结，应有尽有。  🌱我将每一个灵感瞬间、每一次深入思考都记录在此，并通过黑曜石强大的双向链接功能，让这些知识相互交织，形成独一无二的知识网络。💡这不仅帮助我高效整理思绪、回顾过往经验，还能助力我快速找到解决问题的灵感。它见证了我一路以来的成长与进步✨</p>
      </div>
    </div>
    <!-- 天气信息 -->
    <div style=" width: 100%; height:100;overflow: hidden; margin-top: 10px;">
      <iframe src="https://widget.pkmer.cn/free/miniTianqi?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&select-theme=ta&theme=%E6%A0%B7%E5%BC%8F5&input-text=&theme-color=%2320F8FFFF&select-icon=gif" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe>
    </div>
  </div>
  <!-- 右侧栏 -->
  <div style="width: 48%;">
    <div style=" width: 90%;  height:680px;transform: scale(0.6); margin-top:-160px;;overflow: hidden; ">
      <iframe src="https://widget.pkmer.cn/free/Space?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe>
    </div>
  </div>
</div>

![[⏲️时间进度仪表板]]

--- start-multi-column: ID_5 fg 3
```column-settings
Number of Columns: 3
Largest Column: standard
```


![[个人时间表#日常时间管理]]


--- column-break ---



```dataview
table file.mday
SORT file.mtime DESC 
limit 21
```


--- column-break ---


![[Dataview（🌤️天气预报🌦️）#天气预报]] >


--- end-multi-column