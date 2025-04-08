---
tags: []
aliases:
  - dataview
rating: "4"
date: 2024年8月9日
---
## 01 简单示例
```dataview
Table file.ctime as "创建日期"
where date(today) - file.ctime <= dur(3 day)
sort file.ctime desc
```

![[Pasted image 20240809151659.png]]
## 10 Metadata 数据
- ~ Metadata 关于数据的数据（中介数据）描述数据信息信息的数据
- ! [Key Value] : 一个键值对 ，Key 称为 属性名 ；Value 称为 属性域 这种数据对是一种天然的索引

```dataview
Table this
where file = this.file
```
![[Pasted image 20240809152523.png]]
作者:: 李成龙
[读者:: 李成龙]
(读者:: 李成龙)


### Ref 
1. [Obsidian插件-Dataview强大的数据处理和查询功能](https://mp.weixin.qq.com/s/zKtmNmuOdv6KP3QLX_OTtw)
2. [Obsidian插件-Dataview：强大的数据查询和展示工具](https://mp.weixin.qq.com/s/hsUEtKiLf2sTSlmEEqSFxA)
3. [JavaScript 教程 | 菜鸟教程](https://www.runoob.com/js/js-tutorial.html)
4. [HTML 教程 | 菜鸟教程](https://www.runoob.com/html/html-tutorial.html)
5. [CSS 教程 | 菜鸟教程](https://www.runoob.com/css/css-tutorial.html)
6. [YAML 入门教程 | 菜鸟教程](https://www.runoob.com/w3cnote/yaml-intro.html)
7. [Obsidian 插件之 Dataview - 少数派](https://sspai.com/post/68183)