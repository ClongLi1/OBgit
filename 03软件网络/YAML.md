--
# 0. 引言
>[!note] YAML 语法规则
>- 大小写敏感，可以使用中文；
>- 冒号后要跟一个空格；
>- 使用缩进来代表层级关系；
>- 缩进时只能用空格，不能用 Tab；
>- 缩进的空格数不重要，但是同一级元素必须左对齐；
>- 用井号标识注释，从 `#` 到当前行的末尾是注释

> [!warning] YAML 语法注意事项
> - 如果你的 YAML 格式正确，则阅读模式下会自动隐藏，否则会标红报错；
> - 占位符里的冒号后有空格，如 {{time: HH:mm}} ，留意占位符里的 time,或者 date 冒号后面也是要添加一个空格的；
> - 可以使用所有字符作为键 or 值（包括 emoji 在内），但若放在键的位置，则仍需要放入中括号中，除了 task 的情况；
> - dv 检索时，原关键字的值的格式必须正确，否则 dv 会报错，但这种情况下不是代码写错了，而是代码检索的对象有问题；

# 1. 学习笔记
 1. [[YAML语言教程（BILIBILI）]]
 2. [[一个YAML实例]]
 3. [一文看懂 YAML - 知乎](https://zhuanlan.zhihu.com/p/145173920)




---
### Ref
1. [轻松掌握YAML语言、语法_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1yd4y1X75D/?spm_id_from=333.337.search-card.all.click&vd_source=d1167fc706d8bb4a356a82d19d9d3304)
2. https://www.runoob.com/w3cnote/yaml-intro.html
3. [一文看懂 YAML - 知乎](https://zhuanlan.zhihu.com/p/145173920)