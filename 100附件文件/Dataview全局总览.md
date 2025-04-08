```dataview                          
TABLE  dateformat(file.mtime, "yyyy-MM-dd") AS "最后修改日期", file.words AS "字数", file.size AS "文件大小 (字节)", file.folder AS "文件夹路径" FROM "" WHERE file.mtime >= date(now) - dur(3 days) SORT file.mtime DESC  
LIMIT 10
```
