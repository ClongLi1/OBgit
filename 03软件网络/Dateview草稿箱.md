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

