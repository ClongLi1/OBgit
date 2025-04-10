## 1. 距离毕业
```dataviewjs
// 设置目标日期（例如：2024-12-31）
const targetDate = new Date("2025-12-31").getTime();

// 获取当前日期
const currentDate = dv.current.date.getTime();

// 计算剩余时间（毫秒）
const timeRemaining = targetDate - currentDate;

// 将毫秒转换为天、小时、分钟和秒
const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
const hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
const minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
const seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);

// 输出倒计时
dv.paragraph(`
距离目标日期还有：
**${days}天 ${hours}小时 ${minutes}分钟 ${seconds}秒**
`);
```
