```dataview
table 
  file.name as "文件名", 
  file.outlinks as "外部链接", 
  file.inlinks as "内部链接", 
  file.cday as "创建日期", 
  file.mday as "修改日期", 
  file.size as "文件大小 (字节)", 
  file.wordcount as "字数", 
  file.tags as "标签", 
  file.folder as "文件夹路径"
from ""
sort file.cday desc
```