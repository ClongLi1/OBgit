```dataviewjs
var i = [dv.pages().length,dv.pages(`"00科研相关"`).length,dv.pages(`"03软件网络"`).length,
         dv.pages().file.etags.distinct().length]
dv.paragraph(`总共有 **${i[0]}** 个文件`)
dv.paragraph(`==标签== **${i[3]}**个`)
dv.paragraph(`其中科研相关笔记 **${i[1]}** 篇，软件网络相关 **${i[2]}** 篇`)

```
```da'ta
```