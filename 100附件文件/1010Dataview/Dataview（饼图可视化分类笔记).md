```dataviewjs
let la = ""
let da = ""
for(let i of dv.pages().groupBy(p=>p.file.folder.split("/")[0]))
{
	if(i.key=='') la += "/,";
	else la += i.key + ",";
	da += i.rows.length + ",";
}

dv.paragraph(`\`\`\`chart
type: pie
labels: [${la}]
series:
- title: none
  data: [${da}]
width: 50%
legendPosition: left
labelColors: true
\`\`\``);
```
