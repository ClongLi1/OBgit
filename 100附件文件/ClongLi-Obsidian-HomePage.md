

<div style=" width: 100%; height:280;overflow: hidden; "><iframe src="https://widget.pkmer.cn/free/Carousel?user=a2e5899e-975e-4457-afd4-ec3ff7dcbc90&" allow="fullscreen" style=" height: 100%; width: 100%;"></iframe></div>

```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));
let totalDays = `<span style='color:#00FFD7'>🌅我已在**[[Obsidian]]**的知识宇宙中穿行</span> <span style='color:#00FFD7'>${total}天💥，</span>`;
let nofold = '!"misc/templates"';
let allFile = dv.pages(nofold).file;
let totalMd = `<span style='color:#00FF55'>已成功点亮</span> <span style='color:#00FF55'>${allFile.length}</span> <span style='color:#00FF55'>颗璀璨✨星辰笔记</span>`;
let tagDescription = `<span style='color:#FFA933'></span>`;
let totalTag = `<span style='color:#FFFF00'>精心打造了${allFile.etags.distinct().length}</span> <span style='color:#FFFF00'>个标签🫧轨道，</span> ${tagDescription}`;
let taskDescription = `<span style='color:#E610FF'>待办任务等待点亮✨它们宛如纽带，串联起不同星体🌈，让整个星系紧密相连🎆</span>`;
let totalTask = `<span style='color:#E610FF'>还有${allFile.tasks.length}</span> <span style='color:#FF8C00'>个</span> ${taskDescription}`;

dv.paragraph(totalDays + totalMd + "、" + totalTag + "、" + totalTask);
```

```contributionGraph
title: ""
graphType: default
dateRangeValue: 810
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

```dataviewjs
const today = new Date();
const currentMonth = today.getMonth(); // 0 = January, 11 = December
const currentDay = today.getDate();
const currentMonthName = today.toLocaleString('default', { month: 'long' });
const currentDayName = today.toLocaleDateString('zh-CN', { weekday: 'long' });

// 计算当前日期在一年中的位置（百分比）
const daysInMonth = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31];
let totalDays = 0;
for (let i = 0; i < currentMonth; i++) {
  totalDays += daysInMonth[i];
}
totalDays += currentDay;

const totalYearDays = 365; // 非闰年
const positionPercentage = (totalDays / totalYearDays) * 100;

// 创建时间轴
let timeline = "";
timeline += `<div style="display: flex; height: 20px; margin: 20px 0; position: relative;">`;

// 为每个月创建一个div
const monthColors = [
  "#FF0000", "#FF7F00", "#FFFF00", "#00FF00", 
  "#0000FF", "#4B0082", "#8B00FF", "#FFC0CB", 
  "#00FFFF", "#FFD700", "#800080", "#A52A2A"
];

for (let i = 0; i < 12; i++) {
  timeline += `<div class="month-segment" style="flex: 1; background-color: ${monthColors[i]}; height: 100%;"></div>`;
}

timeline += `</div>`;

// 添加指针标记
timeline += `<div style="position: absolute; top: 30%; transform: translate(-50%, -50%); 
  left: ${positionPercentage}%; z-index: 10; display: flex; flex-direction: column; align-items: center;">`;
timeline += `<div style="width: 0; height: 0; border-left: 10px solid transparent; 
  border-right: 10px solid transparent; border-top: 20px solid #000000;"></div>`;
timeline += `<div style="margin-top: 5px; font-size: 12px; color: #333; white-space: nowrap;">`;
timeline += `${currentMonthName} ${currentDay}日，${currentDayName}`;
timeline += `</div>`;
timeline += `</div>`;

// 添加月份标签
timeline += `<div style="display: flex; justify-content: space-between; margin-top: 10px; font-size: 12px; color: #888;">`;
timeline += `<div>January</div>`;
timeline += `<div>February</div>`;
timeline += `<div>March</div>`;
timeline += `<div>April</div>`;
timeline += `<div>May</div>`;
timeline += `<div>June</div>`;
timeline += `<div>July</div>`;
timeline += `<div>August</div>`;
timeline += `<div>September</div>`;
timeline += `<div>October</div>`;
timeline += `<div>November</div>`;
timeline += `<div>December</div>`;
timeline += `</div>`;

dv.el("div", timeline);

// 每天自动更新
setInterval(() => {
  location.reload();
}, 24 * 60 * 60 * 1000); // 每24小时刷新一次
```

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
setting.headerLevel = 3;//添加标题的等级
setting.addDesc = true;//是否添加描述
setting.onlyToday = false;//是否只在当天显示
setting.anotherCity = "内乡";//添加另外一个城市

//脚本文件 weatherView.js 所在路径
dv.view("100附件文件/weatherView",setting)
```

