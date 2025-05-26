# 1. 多级标题 （一级标题）
## 1.1 二级标题
### 1.3 三级标题 
#### 1.4 四级标题 
##### 1.5 五级标题 
###### 1.6 六级标题 
---
# 2. 文本元素 

这是一段文字
*这是一段文字（斜体）*
**这是一段文字（粗体**
***这是一段文字（粗斜体**
==只是一段文字（高亮）==
~~这是一段文字（删除文本）~~
这是一个行内代码 `ctrl`
>  这是一段引用（长风破浪会有是，直挂云帆济沧海）

---
# 3. 表格-图片-视频-录音-公式- 代码 
## 3.1 表格
| 表头 |表头  | 表头 |
|:---|:---|:---|
| 表格元素 |  表格元素|表格元素  |
|表格元素  |表格元素  |  表格元素|  

## 3.2 图片 (大小、位置、图床)
![image.png|600](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20250526121408.png)

## 3.3 视频（Bilibili、Youtube 支持播放）
<iframe src="http://player.bilibili.com/player.html?isOutside=true&aid=114543959216125&bvid=BV15WJqzcEgE&cid=30068838000&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width=80% height=600 ></iframe>

## 3.4 公式 (LaTeX )

$$ f(x) = a - b \tag{1.1} $$

$$\sqrt{x} + \sqrt{x^{2}+\sqrt{y}} = \sqrt[3]{k_{i}} - \frac{x}{m} \tag{1.2}$$


$$\begin{bmatrix}
1 & 2 & \cdots \\
67 & 95 & \cdots \\
\vdots  & \vdots & \ddots \\
\end{bmatrix} \tag{1.3}$$


## 3.5 代码块（各种编程语言） 

```LaTeX
$$\begin{bmatrix}
1 & 2 & \cdots \\
67 & 95 & \cdots \\
\vdots  & \vdots & \ddots \\
\end{bmatrix}$$
```

```Python
#!/usr/bin/python
# -*- coding: UTF-8 -*-
 
for i in range(1,5):
    for j in range(1,5):
        for k in range(1,5):
            if( i != k ) and (i != j) and (j != k):
                print (i,j,k)
```

## 3.6 录音（打字慢？直接录音）
**这是一段录音**
![[Recording 20250526122255.m4a]]

---
# 4. 有序、无序、待办列表 
## 4.1 有序列表 
1. 第一吧啦吧啦布拉吧
2. 第二吧啦吧啦布拉吧
3. 第一吧啦吧啦布拉吧

## 4.2 无序列表
- 要点 1 啊啊啊啊
- 要点 1 啊啊啊啊
- 要点 1 啊啊啊啊

## 4.3 待办列表 

- [ ] 任务事项 （未完成）
- [ ] 任务事项 （未完成）
- [ ] 任务事项 （未完成）
- [x] 任务事项 （已完成） ✅ 2025-05-26
- [x] 任务事项 （已完成） ✅ 2025-05-26
---
# 5. 内部链接和外部链接 
## 5.1 内部链接 （Obsidian 最大亮点）
```源码
[[标题]]    （链接另一篇笔记）
！[[标题 ]] （在当前笔记，显示另一篇笔记）
[[标题|别名]] （给笔记起一个新的名字）
![[另一篇笔记]] 
[[标题#章节]]
[[标题^ 某一片段]] （链接笔记中某一具体片段）
```

[[Obsidian语法]] (不显示内容)

![[Obsidian语法]] （预览内容）

 ![[Obsidian语法#1. 标题]] (预览某一章节)

## 5.2 外部链接 （可直接预览）
这是哔哩哔哩的网址[哔哩哔哩 (゜-゜)つロ 干杯\~-bilibili](https://www.bilibili.com/)

# 6. 高亮块及分栏 

```Callout 语法格式
>[!字符]
> 内容 BaLaBaLa......

 字符内容：
- note
- abstract, summary, tldr
- info, todo
- tip, hint, important
- success, check, done
- question, help, faq
- warning, caution, attention
- failure, fail, missing
- danger, error
- bug
- example
- quote, cite
```

> [!note]  (note、abstract、bug、info、example、tip...)
> 1. 用于显示重点内容
> 2. 用于总计提炼要点 


--- start-multi-column: ID_ivuh
```column-settings
Number of Columns: 4 
Largest Column: standard
```

> [!tip]  
> - 这是一个建议
> - 这是一个建议
> - 这是一个建议

--- column-break ---

> [!example]  这是例子
> 1. 例子 aaaaaa
> 2. 举例 bbbbb 
> 3. 其它 cccccc

--- column-break ---

> [!bug]  这是例子
> 1. 例子 aaaaaa
> 2. 举例 bbbbb 
> 3. 其它 cccccc

--- column-break ---

> [!todo]  这是例子
> 1. 例子 aaaaaa
> 2. 举例 bbbbb 
> 3. 其它 cccccc

--- end-multi-column

---
# 7. 脚注 （支持预览）
这是一个脚注（用于解释说明）[^1]
这是脚注（可以是外部网址链接）[^2]
这是脚注（可以预览内容）[^3]


[^1]: 这是脚注，可以是文字备注
[^2]: [Fetching Title#70sw](https://www.bilibili.com/)
[^3]: 长风破浪会有是，直挂云帆济沧海

---

# 8. 嵌入页面（预览访问）

```
<iframe width=600 height=400 src="页面链接地址" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```

<iframe width=600 height=400 src="https://www.runoob.com/html/html-tutorial.html" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

---

# 9. 漂亮的 Callout 
- $ 提示 
- ~ 提示
- ! 提示
- % 提示 
- & 提示 
- @ 提示 

---

# 10. Mermaid (各种导图、流程图、饼图)

![[Mermaid图表类型举例]]
