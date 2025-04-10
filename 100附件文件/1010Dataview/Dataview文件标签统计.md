```dataviewjs
var i = [dv.pages().length,dv.pages(`""`).length,dv.pages(`"700-收集文章"`).length,
         dv.pages().file.etags.distinct().length]
dv.paragraph(`总共有 **${i[0]}** 个文件`)
dv.paragraph(`其中==笔记== **${i[1]}** 篇，==收集文章== **${i[2]}** 篇`)
dv.paragraph(`==标签== **${i[3]}**个`)
```
