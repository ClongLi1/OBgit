---
aliases:
  - Dataview语法
tags: []
等级: ⭐⭐⭐
---

# 0. 引言


# 1. Dataview 基本语法
## 1.1 简单示例
[[dataview 测试文件]]
> [!tip ] dataview
> Table\list
> Where
> Sort


- $ REF: [PKMer_一个 Dataview 查询示例](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/dataview/dataview%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95/01---%E7%AE%80%E5%8D%95%E7%A4%BA%E4%BE%8B/)
---
## 1.2 Dataview 中的 [[Metadata]] 元数据

- @ [PKMer_Dataview 中的Metadata元数据](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/dataview/dataview%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95/10---metadata-%E5%85%83%E6%95%B0%E6%8D%AE/)
---
## 1.3 文档属性和行内字段

- ~ [PKMer_Dataview：向文件添加合适的元数据](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/dataview/dataview%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95/11---%E6%B7%BB%E5%8A%A0%E5%85%83%E6%95%B0%E6%8D%AE%E8%87%B3%E6%96%87%E4%BB%B6/)
---
## 1.4 向列表和任务添加元数据
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20241228173342.png)
[📆:: 2024 年 12 月 28 日]
[✅:: 2024 年 12 月 28 日]
[✈️:: 2024 年 12 月 28 日]
[➕:: 2024 年 12 月 28 日]
[⏳:: 2024 年 12 月 28 日]

---
## 1.5 [[Metadata]] 的数据类型

---
# 2. Dataview 案例
## 2.1 显示当前文件的所有元数据
```d
table this
where file = this.file
```
### Ref
 