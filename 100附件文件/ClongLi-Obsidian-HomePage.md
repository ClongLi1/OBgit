---
banner: "![[a.webp]]"
Banner_y: 0.886
banner_y: 0.664
---
<div style=" width: 100%; height: auto;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/YearTimeline?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe></div>

  ```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
  let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000));
  let totalDays = " <span style='color:#00FFD7'>🌅我已在`Obsidian`的知识宇宙中穿行"+total+"</span> <span style='color:#00FFD7'>天💥，</span>";
  let nofold = '!"misc/templates"';
  let allFile = dv.pages(nofold).file;
  let totalMd = "<span style='color:#00FF55'>已成功点亮 </span><span style='color:#00FF55'>"+allFile.length+"</span><span style='color:#00FF55'> 颗璀璨✨星辰笔记</span>";
  let tagDescription = "<span style='color:#FFA933'>它们宛如纽带，串联起不同星体🌈，让整个星系紧密相连🎆</span>";
  let totalTag = "<span style='color:#FFFF00'>精心打造了"+allFile.etags.distinct().length+"</span><span style='color:#FFFF00'> 个标签🫧轨道，</span>"+tagDescription;
  dv.paragraph(totalDays+totalMd+"、"+totalTag+"");
  
``` 
```contributionGraph
title: ""
graphType: default
dateRangeValue: 800
dateRangeType: LATEST_DAYS
startOfWeek: 1
showCellRuleIndicators: true
titleStyle:
  textAlign: center
  fontSize: 20px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField:
    format: yyyy-mm-dd-tt
fillTheScreen: true
enableMainContainerShadow: false
mainContainerStyle: {}
cellStyle:
  borderRadius: ""
  minWidth: 10px
  minHeight: 10px
cellStyleRules:
  - id: default_b
    color: "#ffffccff"
    min: "1"
    max: "2"
  - id: default_c
    color: "#ffeb99ff"
    min: "2"
    max: "4"
  - id: default_d
    color: "#ffd700ff"
    min: "4"
    max: "6"
  - id: default_e
    color: "#ffa500ff"
    min: "6"
    max: "8"
  - id: 1740749878263
    min: "8"
    max: "10"
    color: "#ff4500ff"
    text: ""
  - id: 1740749904057
    min: "10"
    max: "99"
    color: "#ff0000ff"
    text: ""

```
<div style=" width: 100%; height:280;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/Carousel?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe></div>
<div style="display: flex; flex-wrap: wrap; justify-content: space-between;">
  <!-- 左侧栏 -->
  <div style="width: 48%; margin-bottom: 1px;">
    <!-- Obsidian logo 和欢迎语 -->
    <div style="display: flex; align-items: center; margin-bottom: 20px;">
      <img src="Obsidian logo.png" alt="Obsidian Logo" style="width: 230px; height: 320px; margin-right: 20px;">
      <div>
        <h3>✨ 欢迎来到我的 Obsidian 知识库🌟</h3>
        <p>🔥这里是我的个人数字花园，更是我精心打造的知识宝库。在这个库里，你可以发现各种各样的笔记，💗从工作中的项目规划、行业动态分析，到个人成长中的读书心得、技能学习总结，应有尽有。  🌱我将每一个灵感瞬间、每一次深入思考都记录在此，并通过黑曜石强大的双向链接功能，让这些知识相互交织，形成独一无二的知识网络。💡这个库不仅帮助我高效整理思绪、回顾过往经验，还能助力我快速找到解决问题的灵感。它见证了我一路以来的成长与进步，相信也会成为你探索知识、激发创意的好帮手。 🚀快来一起探索吧！✨</p>
      </div>
    </div>
    <!-- 天气信息 -->
    <div style=" width: 100%; height:100;overflow: hidden; margin-top: 10px;">
      <iframe src="https://widget.pkmer.cn/free/miniTianqi?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&select-theme=ta&theme=%E6%A0%B7%E5%BC%8F4&input-text=&theme-color=%2350F9FFFF&select-icon=durian" allow="fullscreen" style=" height: 150%; width: 150%;"></iframe>
    </div>
  </div>
  <!-- 右侧栏 -->
  <div style="width: 48%;">
    <div style=" width: 90%;  height:680px;transform: scale(0.6); margin-top:-160px;;overflow: hidden; ">
      <iframe src="https://widget.pkmer.cn/free/Space?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe>
    </div>
  </div>
</div>

```dataviewjs
let setting = {};

//在和风天气中创建的 Api key
setting.key = "e432e1a280d344cd89befe667f366400";

setting.city = "山阳";//城市名
setting.days = 7;//天气预报天数
setting.headerLevel = 1;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = false;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```

