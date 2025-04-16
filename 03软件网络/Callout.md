
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
![[Recording 20240116092813.webm]]

## 4.2 嵌入视频
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
