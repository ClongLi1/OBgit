```dataviewjs
// 获取所有非隐藏文件夹（排除系统文件夹） 
const folders = Array.from(new Set( dv.pages().file.folder .filter(f => f && !f.startsWith(".")) 
// 排除隐藏文件夹 
.map(f => f.split("/")[0]) // 获取一级目录 
)); 
// 构建数据对象 
const data = folders.map(folder => ({ name: folder, count: dv.pages(`"${folder}"`).length })); 
// 转换为Charts插件需要的格式 
const labels = data.map(x => x.name); const counts = data.map(x => x.count); 
// 渲染图表 
dv.paragraph(`\`\`\`chart type: pie labels: [${labels.map(l => `"${l}"`).join(",")}] series: - title: "笔记数量" data: [${counts.join(",")}] width: 90% labelColors: true \`\`\``);
```

```chart
type: pie 
labels: ["00-闪念笔记","00写作运营","00科研相关","00草稿收集","01生活方面","02专业知识","03软件网络","04方法思维","05工作职场","06口才社交","07文学历史","08灵感梦想","09心灵慰藉","10001AI写作","10001电商运营","100附件文件","10总结反思","11情感婚恋","12亲子教育","13英语相关","14运动医学","15-琐碎问题","16-时政现实","99-必备技能","998日记汇总","999知识管理","export","轻研企业写作"] 
series: - 
title: "笔记数量" 
data: [4,28,30,27,32,77,99,45,36,6,38,3,13,2,1,28,36,9,3,23,4,2,8,8,76,4,5,1] 
width: 90% 
labelColors: true
```


```dataviewjs
const threshold = 15; // 聚合阈值 
const data = { "闪念笔记": 4, "写作运营": 28, "科研相关": 30, // ... 其他原始数据 
"其他": [1,3,2,4,5].reduce((a,b)=>a+b) // 手动聚合小类 
};
 dv.paragraph(`\`\`\`chart 
 type: pie 
 labels: [${Object.keys(data).map(k => `"${k}"`)}] 
 series: 
 - title: "聚合后笔记分布" 
 data: [${Object.values(data)}] 
 options: 
  plugins: 
  	tooltip: 
  		enabled: true # 开启hover提示细节 
  		width: 95%
  		 \`\`\``);
```
