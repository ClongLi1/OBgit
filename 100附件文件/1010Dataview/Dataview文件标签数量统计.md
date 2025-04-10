```dataviewjs
// 获取今天的日期
const today = new Date();
const todayStr = `${today.getFullYear()}-${today.getMonth() + 1}-${today.getDate()}`;
const daysUsed = Math.floor((today - new Date("2024-07-01")) / (1000 * 60 * 60 * 24));

// 获取文件夹名称和颜色
const folders = [
    { name: "00科研相关", color: "#FF6384" },
    { name: "00写作运营", color: "#36A2EB" },
    { name: "01生活方面", color: "#FFCE56" },
    { name: "02专业知识", color: "#4BC0C0" },
    { name: "03软件网络", color: "#9966FF" },
    { name: "04方法思维", color: "#FF9966" },
    { name: "05工作职场", color: "#CC3333" },
    { name: "06口才社交", color: "#66CC99" },
    { name: "07文学历史", color: "#FFCC00" },
    { name: "08灵感梦想", color: "#993366" },
    { name: "09心灵慰藉", color: "#6699CC" },
    { name: "10总结反思", color: "#CC99FF" },
    { name: "11情感婚恋", color: "#FF66CC" },
    { name: "12亲子教育", color: "#339966" },
    { name: "13英语相关", color: "#FF6600" },
    { name: "14运动医学", color: "#666699" },
    { name: "15-琐碎问题", color: "#99CC00" },
    { name: "16-时政现实", color: "#CC6600" },
    { name: "99-必备技能", color: "#0099CC" }
];

// 获取总笔记数、总标签数
const totalNotes = dv.pages().length;
const totalTags = dv.pages().file.etags.distinct().length;

// 输出使用天数、总笔记数和总标签数
dv.paragraph(`我已经使用Obsidian：**<span style="color: #FF6384;">${daysUsed}</span>**天，总笔记数：**<span style="color: #36A2EB;">${totalNotes}</span>**篇，总标签数：**<span style="color: #FFCE56;">${totalTags}</span>**个`);

// 创建一个列表来展示文件夹统计信息
dv.list(folders.map(folder => {
    const count = dv.pages(`"${folder.name}"`).length;
    return `**<span style="color: ${folder.color};">${folder.name}</span>**：**${count}**篇`;
}), "unordered");
```

```dataviewjs
let la = Array()
let da = Array()
for(let i of dv.pages().groupBy(p=>p.file.folder.split("/")[0]))
{
	la.push(i.key);
	let n = dv.pages(`"${i.key}"`).length;
	da.push(n);
}

dv.paragraph(`\`\`\`chart
type: pie
labels: [${la}]
series:
- title: 
  data: [${da}]
width: 50%
legendPosition: left
labelColors: true
\`\`\``);
```

