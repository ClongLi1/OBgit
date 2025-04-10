```dataview                          
TABLE without id dateformat(file.mtime, "yyyy-MM-dd") AS "最后修改日期", file.folder AS "文件夹路径" FROM "" WHERE file.mtime >= date(now) - dur(3 days)
SORT file.mtime DESC  
LIMIT 10
```
