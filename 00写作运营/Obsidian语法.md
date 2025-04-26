---
aliases: []
---
### 1. 标题
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
### 脚注
长风破浪会有时，直挂云帆济沧海。[^1]
你可以使用 `[^脚注标识]` 来插入脚注，然后在文档的任何地方使用 `[^脚注标识]: 脚注内容` 来定义脚注。例如，`这是一个脚注[^1]` 和 `[^1]: 这是脚注的内容` 会创建一个带有脚注的文本

### 标签
`#标签`
`#标签/镶嵌标签`

### 语法块
> [!help] 这是一个高亮块
>> [!seealso] 镶嵌进去
> 

```ad-note
这是一个笔记
```

> [!note|cite] 
> 李成龙李成龙
> 
> 李成龙
### 数学公式
```
$$
\begin{aligned}
\frac{\partial f}{\partial x} =0 \\
\frac{\partial f}{\partial y} =0
\end{aligned}
$$
```
$$
\begin{aligned}
\frac{\partial f}{\partial x} =0 \\
\frac{\partial f}{\partial y} =0
\end{aligned}
$$
### 分割线
```
---
***
```
***
### 引用
```
> 这段是引用
>>  嵌套引用
```

> 这是一段引用
>>  嵌套引用
---
### 内部链接
```
[[标题]] 
[[标题 ]]
[[标题|别名]]
![[另一篇笔记]]
[[标题#章节]]
```
-  [Obsidian新手全面入门09-共搭个人知识库-双向链接](https://mp.weixin.qq.com/s/JXRALuK48waWoh9Py285Og)
### 外部链接
```
[百度](www.baidu.com）
```
### 文本
```
文本
**加粗**
*斜体*
***粗斜***
```

### 视频
```
<iframe src="https://player.bilibili.com/player.html?aid=702374093&bvid=BV1Xm4y1n7bQ&cid=1232824646&page=1&autoplay=false" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="80%" height="500"> </iframe>
```
### 录音（自带）

![[Recording 20250104145320.webm]]
### 高亮块
```
> [!note] 这是主图 （note tip abstract warning example bug info ）
> 正文吧啦吧啦...

```

> [!note] 这是高亮块
> 这是一个高亮块

### 列表
```
有序列表
1. 
2. 
3. 
```

```
无序列表
- aaa
- aaa
-  
```

```
任务列表
- [] 任务1
- [] 任务2
```
### 代码块
```
行间代码
```

`行内代码`

### 注释内容
```
<!-- 注释内容 -->
%% 这是注释内容 %%
```
<!-- 注释内容 -->
%% 这是注释内容 %%

# 图片
直接复制粘贴
图床超链接（类似一个网址）

# 表格 (借助插件)
```
| 行/列 | 列名2 | 列明3 |
| ----- | ----- | ----- |
| 行名1 |       |       |
| 行名2 |       |       |
| 行名3 |       |       |
```


# 1. Callout 


```
Callout 语法格式
>[!字符]
> 内容 BaLaBaLa......
```
 ```
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
[[Callout]]

```
ad-tip

```
```ad-bug
这是bug
```
```
> [!quote|cite] 正所谓
> 一句名人名言
> 
> 谁说的

```

> [!tip|cite] 
>  长风破浪会有时，直挂云帆济沧海。
>  
> 李成龙
# 2. YAML
- `title`: 这定义了笔记的标题，有时这个标题会在图表视图或链接的预览中替代文件名显示。
- `tags`: 这是笔记相关的标签列表，标签通常用于组织和搜索笔记。
- `aliases`: 这是笔记的别名列表，利用别名可以使您用不同的名称引用同一笔记。
- `created`: 这指明了笔记创建的日期。
- `modified`: 这表示笔记上次修改的日期。 
- `author` 来标识作者 
- `status` 来标识笔记状态等
- `Category`: "知识管理"
- `Summary`: "这是关于 YAML 头部使用的一个示例笔记。
- `priority`: "高"

# 3. Excalidraw 
1. [Obsidian-Excalidraw 功能手册](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/excalidraw/obsidian-excalidraw-%E5%8A%9F%E8%83%BD%E6%89%8B%E5%86%8C/)


# 4. Iframe 嵌入语法
## 4.1 嵌入音频
1. 录音功能

![[Recording 20250420123514.m4a]]

## 4.2 嵌入
```
<video width="600" height="420" controls> 
<source src="movie.mp4" type="video/mp4"> 
<source src="movie.ogg" type="video/ogg">
<source src="movie.webm" type="video/webm"> 
</video>
```

>- **说明：**
    - Width ( 宽度 ) height ( 高度 ) ，可以自己设置，直接输入数字即可，单位默认是 px (像素)  
        也可以使用 **百分比**  
        **`width=100%`** 代表水平撑满整个窗口  
        **`height=50%`** 代表垂直撑满半个窗口
    - **Video 标签** 支持的视频格式 ：MP 4 ogg webm
## 4.3 嵌入页面
```
<iframe width=600 height=400 src="页面链接地址" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
```
<iframe width=600 height=400 src="https://www.runoob.com/html/html-tutorial.html" scrolling="auto" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
## 4.4 嵌入在线视频
1.  [如何插入视频网站视频？](https://www.wolai.com/wolai/go85vJpt3wDwrid7DfCZcE)
2. <iframe src="https://player.bilibili.com/player.html?aid=538308832&bvid=BV1ni4y1z7ha&cid=1394161464&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
3. <iframe src="https://player.bilibili.com/player.html?aid=283578411&bvid=BV1Pc411b74G&cid=1402019060&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

# 5. Mermaid

## REF

[^1]: 源于李白《蜀道难》
- [Markdown | 让文本更加精致【语法篇】](https://mp.weixin.qq.com/s/mxwDk2p0G_NycF6JMJRnew)
- 