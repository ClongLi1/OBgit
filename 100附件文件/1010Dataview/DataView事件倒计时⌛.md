
```dataviewjs
// 设置目标日期（例如：2024-12-31）
const targetDate = new Date("2025-06-20").getTime();

// 获取当前日期
const currentDate = new Date().getTime();

// 计算剩余时间（毫秒）
const timeRemaining = targetDate - currentDate;

// 将毫秒转换为天
const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));

// 输出倒计时
dv.paragraph(`
1. 距离硕士毕业还有日期还有：**${days}天**
`);
```
```dataviewjs
// 设置事件名称和目标日期
const event = "某事件";
const targetDate = new Date("2026-01-01").getTime();

// 获取当前日期
const currentDate = new Date().getTime();

// 计算剩余时间（毫秒）
const timeRemaining = targetDate - currentDate;

// 将毫秒转换为天
const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));

// 输出倒计时，使用不同颜色和加粗
dv.paragraph(`
2. 距离**<span style="color: red;">新春佳节</span>**还有：**<span style="color: yellow;">${days}</span>**天
`);
```
