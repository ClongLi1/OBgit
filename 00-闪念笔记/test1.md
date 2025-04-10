


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
  	 enabled: true  
width: "95%"  
 \`\`\``);  
```
