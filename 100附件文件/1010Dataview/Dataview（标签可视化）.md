```dataviewjs
let la = "";
let da = "";
let map = dv.index.tags.invMap;

for (let i of map.entries()) {
    if (i[1].size > 5) { 
        la += i[0].slice(1) + ",";
        da += i[1].size + ",";
    }
}

dv.paragraph(`\`\`\`chart
type: pie
labels: [${la}]
series:
- title: none
  data: [${da}]
legendPosition: left
labelColors: true
\`\`\``);
```