```dataviewjs
// 修复版：安全访问标签数据 + 容错处理 
const tags = dv.app.metadataCache.getTags() || new Map(); 
const invMap = tags.invMap || new Map(); 

let labels = []; 
let data = []; 
if (invMap.size > 0) { 
	for (const [tag, pages] of invMap) { 
		if (pages.size > 1 && tag.startsWith("#")) { 
			labels.push(tag.slice(1)); 
			data.push(pages.size); 
		} 
	} 
} 
if (labels.length > 0) { 
	dv.paragraph(`\`\`\`chart 
	type: pie 
	title: 多标签统计 
	labels: [${labels}] 
	series: 
		- data: [${data}] 
		legendPosition: right innerRadius: 40% labelColors: true \`\`\``); } else { dv.paragraph("✅ 无重复标签或需要更新索引\n> 执行 `Dataview: Update Index` 后重试"); }
```