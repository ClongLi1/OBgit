---
tags:
  - a
---
```
```dataview
list 
from #Dataview 
```

```dataview
list 
from #Dataview 
```

```dataview
list 
from #Dataview 
where key = "Value"
```
```dataview 
table 
from #Dataview 
where 作者 = "李成龙"
```
```
let ftMd = dv.pages("").file.sort(t => t.cday)[0]
let total = parseInt([new Date() - ftMd.ctime] / (60*60*24*1000))
let totalDays = "您已使用 ***Obsidian*** "+total+" 天，"
let nofold = '!"misc/templates"'
let allFile = dv.pages(nofold).file
let totalMd = "共创建 "+ allFile.length+" 篇笔记"
let totalTag = allFile.etags.distinct().length+" 个标签"
let totalTask = allFile.tasks.length+"个待办。 "
dv.paragraph(
	totalDays + totalMd + "、" + totalTag + "、" + totalTask
)
```

```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));
let totalDays = `<span style='color:#00FFD7'>🌅我已在**[[Obsidian]]**的知识宇宙中穿行</span> <span style='color:#00FFD7'>${total}天💥，</span>`;
let nofold = '!"misc/templates"';
let allFile = dv.pages(nofold).file;
let totalMd = `<span style='color:#00FF55'>已成功点亮</span> <span style='color:#00FF55'>${allFile.length}</span> <span style='color:#00FF55'>颗璀璨✨星辰笔记</span>`;
let tagDescription = `<span style='color:#FFA933'>它们宛如纽带，串联起不同星体🌈，让整个星系紧密相连🎆</span>`;
let totalTag = `<span style='color:#FFFF00'>精心打造了${allFile.etags.distinct().length}</span> <span style='color:#FFFF00'>个标签🫧轨道，</span> ${tagDescription}`;
let taskDescription = `<span style='color:#E610FF'>待办任务如同未完成的星轨，等待你去点亮✨</span>`;
let totalTask = `<span style='color:#E610FF'>还有${allFile.tasks.length}</span> <span style='color:#FF8C00'>个待办。</span> ${taskDescription}`;

dv.paragraph(totalDays + totalMd + "、" + totalTag + "、" + totalTask);
```

```dataviewjs
dv.paragraph("2025年的时间轴，标记了今天的日期：");

// 获取当前日期
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
timeline += `<div style="display: flex; height: 20px; margin: 20px 0;">`;
timeline += `<div style="flex: 1; background-color: #3498db; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #2ecc71; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #27ae60; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #16a085; height: 100%; position: relative;">`;
timeline += `<div style="position: absolute; width: 2px; height: 100%; background-color: red; left: 50%;"></div>`;
timeline += `</div>`;
timeline += `<div style="flex: 1; background-color: #1abc9c; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #f1c40f; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #e67e22; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #e74c3c; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #9b59b6; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #34495e; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #c0392b; height: 100%;"></div>`;
timeline += `<div style="flex: 1; background-color: #7f8c8d; height: 100%;"></div>`;
timeline += `</div>`;

// 添加动态标记点（表情符号）
timeline += `<div style="position: relative; height: 20px; margin-top: -20px; display: flex; justify-content: center;">`;
timeline += `<div style="position: relative; font-size: 24px;">💎</div>`;
timeline += `</div>`;

// 添加日期和星期信息
timeline += `<div style="text-align: center; margin-top: 5px; font-size: 12px; color: #888;">`;
timeline += `${currentMonthName} ${currentDay}日，${currentDayName}`;
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
```


```dataviewjs
dv.paragraph("2025年的时间轴，标记了今天的日期：");

// 获取当前日期
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
timeline += `<div style="position: absolute; top: 50%; transform: translate(-50%, -50%); 
  left: ${positionPercentage}%; z-index: 10; display: flex; flex-direction: column; align-items: center;">`;
timeline += `<div style="width: 0; height: 0; border-left: 10px solid transparent; 
  border-right: 10px solid transparent; border-top: 20px solid ${monthColors[currentMonth]};"></div>`;
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

// 每天00:00自动更新
function scheduleUpdate() {
  const now = new Date();
  const tomorrow = new Date(now);
  tomorrow.setDate(now.getDate() + 1);
  tomorrow.setHours(0, 0, 0, 0);

  const timeUntilTomorrow = tomorrow.getTime() - now.getTime();

  setTimeout(() => {
    location.reload();
    scheduleUpdate(); // 设置下一次更新
  }, timeUntilTomorrow);
}

scheduleUpdate();
```


```dataviewjs
dv.paragraph("2025年的时间轴，标记了今天的日期：");

// 获取当前日期
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
timeline += `<div style="position: absolute; top: 50%; transform: translate(-50%, -50%); 
  left: ${positionPercentage}%; z-index: 10; display: flex; flex-direction: column; align-items: center;">`;
timeline += `<div style="width: 0; height: 0; border-left: 10px solid transparent; 
  border-right: 10px solid transparent; border-top: 20px solid ${monthColors[currentMonth]};"></div>`;
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

#tag1 #tag2 #tag3 


```dataviewjs
const setTime = new Date("2024/6/15 08:00:00");
const nowTime = new Date();
const restSec = setTime.getTime() - nowTime.getTime();
const day = parseInt(restSec / (60 * 60 * 24 * 1000));
dv.paragraph(day + "天");
```

```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));
let totalDays = "使用 *Obsidian* " + "**" + total + "**天，";
dv.paragraph(totalDays);
```

```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));
let totalDays = "使用 *Obsidian* " + "**" + total + "**天，";
dv.paragraph(totalDays);
```

```dataviewjs
let ftMd = dv.pages("").file.sort(t => t.cday)[0];
let total = parseInt([new Date() - ftMd.ctime] / (60 * 60 * 24 * 1000));
let rainbowStyle = "background: linear-gradient(90deg, #FF0000, #FF7F00, #FFFF00, #00FF00, #0000FF, #4B0082, #9400D3); -webkit-background-clip: text; -webkit-text-fill-color: transparent;";
let totalDays = `<span style="${rainbowStyle}">🌅我在**[[Obsidian]]**的世界中已探索 ${total} 天 🌈，</span>`;
let nofold = '!"misc/templates"';
let allFile = dv.pages(nofold).file;
let totalMd = `<span style="${rainbowStyle}">已发现 ${allFile.length} 颗闪耀的笔记星星 ✨</span>`;
let tagDescription = `<span style="${rainbowStyle}">它们被精心分类在 ${allFile.etags.distinct().length} 个彩虹标签中 🌈</span>`;
let totalTag = `<span style="${rainbowStyle}">，${tagDescription}</span>`;
let taskDescription = `<span style="${rainbowStyle}">还有 ${allFile.tasks.length} 个待办任务等待我去完成，它们如同彩虹的纽带，连接着不同的知识领域 🌈</span>`;
let totalTask = `<span style="${rainbowStyle}">，${taskDescription}</span>`;

dv.paragraph(totalDays + " " + totalMd + " " + totalTag + " " + totalTask);
```