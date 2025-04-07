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
dv.header(2, "时间轴");
dv.paragraph("以下是2025年的时间轴，标记了今天的日期：");

// 获取当前日期
const today = new Date();
const currentMonth = today.getMonth(); // 0 = January, 11 = December
const currentDay = today.getDate();
const currentMonthName = today.toLocaleString('default', { month: 'long' });
const currentDayName = today.toLocaleDateString('zh-CN', { weekday: 'long' });

// 检查是否为闰年
const isLeapYear = (year) => {
    return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0);
};
const year = 2025;
const daysInMonth = isLeapYear(year) ? 
    [31, 29, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31] : 
    [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31];
const totalYearDays = isLeapYear(year) ? 366 : 365;

// 计算当前日期在一年中的位置（百分比）
let totalDays = 0;
for (let i = 0; i < currentMonth; i++) {
    totalDays += daysInMonth[i];
}
totalDays += currentDay;
const positionPercentage = (totalDays / totalYearDays) * 100;

// 创建时间轴
let timeline = "";
timeline += `<div style="display: flex; height: 20px; margin: 20px 0;">`;

// 季节颜色
const seasons = [
    { name: "冬季", color: "#7f8c8d" }, // Winter (Dec-Feb)
    { name: "春季", color: "#2ecc71" }, // Spring (Mar-May)
    { name: "夏季", color: "#f1c40f" }, // Summer (Jun-Aug)
    { name: "秋季", color: "#e67e22" }  // Autumn (Sep-Nov)
];

// 设置每个月的季节颜色
const monthColors = [
    "#7f8c8d", "#7f8c8d", "#7f8c8d", // Dec, Jan, Feb
    "#2ecc71", "#2ecc71", "#2ecc71", // Mar, Apr, May
    "#f1c40f", "#f1c40f", "#f1c40f", // Jun, Jul, Aug
    "#e67e22", "#e67e22", "#e67e22", "#e67e22" // Sep, Oct, Nov, Dec
];

for (let i = 0; i < 12; i++) {
    timeline += `<div style="flex: 1; background-color: ${monthColors[i]}; height: 100%; position: relative;">`;
    // 添加红旗标记
    timeline += `<div style="position: absolute; width: 10px; height: 10px; background-color: red; border-radius: 0; top: -5px; left: 50%; transform: translateX(-50%);">🚩</div>`;
    timeline += `</div>`;
}

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
dv.header(2, "文件统计");
dv.paragraph("以下是所有文件的基本信息：");

// 获取所有文件的信息
const allFiles = dv.pages("");

// 创建文件统计显示
let fileStats = "";
fileStats += `<div style="display: flex; flex-direction: column; margin: 20px 0;">`;

allFiles.forEach(file => {
    fileStats += `<div style="display: flex; flex-direction: column; margin-bottom: 10px; background-color: #2c3e50; color: white; padding: 15px; border-radius: 5px;">`;
    fileStats += `<div style="font-size: 18px; font-weight: bold; margin-bottom: 10px;">${file.name}</div>`;
    fileStats += `<div style="margin-bottom: 5px;">`;
    fileStats += `<span style="font-weight: bold;">字数：</span>${file.wordCount}`;
    fileStats += `</div>`;
    fileStats += `<div style="margin-bottom: 5px;">`;
    fileStats += `<span style="font-weight: bold;">创建时间：</span>${file.ctime}`;
    fileStats += `</div>`;
    fileStats += `<div>`;
    fileStats += `<span style="font-weight: bold;">最后修改时间：</span>${file.mtime}`;
    fileStats += `</div>`;
    fileStats += `</div>`;
});

fileStats += `</div>`;

dv.el("div", fileStats);
```
