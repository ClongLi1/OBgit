
```dataviewjs
// 设置事件名称和目标日期
const event = "硕士毕业";
const targetDate = new Date("2025-06-10").getTime();

// 获取当前日期
const currentDate = new Date().getTime();

// 计算剩余时间（毫秒）
const timeRemaining = targetDate - currentDate;

// 将毫秒转换为天
const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));

// 输出倒计时，使用不同颜色和加粗
dv.paragraph(`
1. 距离**<span style="color: cyan;">${event}</span>**还有：**<span style="color: yellow;">${days}</span>**天
`);
```
```dataviewjs
// 设置事件名称和目标日期
const event = "上班入职";
const targetDate = new Date("2025-07-01").getTime();

// 获取当前日期
const currentDate = new Date().getTime();

// 计算剩余时间（毫秒）
const timeRemaining = targetDate - currentDate;

// 将毫秒转换为天
const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));

// 输出倒计时，使用不同颜色和加粗
dv.paragraph(`
2. 距离**<span style="color: cyan;">${event}</span>**还有：**<span style="color: yellow;">${days}</span>**天
`);
```
```dataviewjs
// 获取今天的日期
const today = new Date();
const todayStr = `${today.getFullYear()}-${today.getMonth() + 1}-${today.getDate()} 星期${'日一二三四五六'[today.getDay()]}`;



// 获取当前日期
const currentDate = new Date().getTime();



// 输出今天的日期
dv.paragraph(`**今天的日期： **<span style="color: #36A2EB;">${todayStr}</span>**`);


```
