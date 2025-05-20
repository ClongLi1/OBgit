Log# 1. 引言 
Git 版本控制“版本”、“文件名”、“修改时间”、“修改内容”
分布式版本控制软件 
## Git 工作流程 
1. 本地建立文件夹（`git init`) 建立 Git 仓库
2. 建立文件（abc. Txt）
3. `git add abc.txt ` (把指定文件（abc. Txt）代码提交暂存区)
4. `git add .` (把所有文件提交到暂存区)
5. `git commit` (提交到仓库)、`git commit -m "备注信息"` 【先 git add 再 git commit 】
6. `git log` (查看节点)
	1. `git log --stat`（查看具体修改内容、关注 `commit`）
	2. `git diff [commit ID]`
	3. `git reset --hard [commit id]` （将代码回退到指定的节点）
	4. `git checkout [commit id]` 将代码回退到指定的节点
7. `git reset --hard HEAD~X` 退回之前版本
8. Git 完成提交的三个内容：==修改文件内容、Git add、Git commit==
9. Git 可视化工具 
10. `git branch` 
11. `git checkout -b 分支` （创建分支）
12. `git checkout 分支名` （切换分支）
13. `git merge` (合并分支)

## Git 远程
1. `git push origin mian` (同步到远程)
2. `git pull origin master` (拉取远程)
![image.png|400](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20250319184848.png)
![image.png|800](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20250319185327.png)


# 待合并
[2024码路 Git实用教程 | Git | 码路 | 全栈 | 培训\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1rK42147su/?spm_id_from=333.999.0.0&vd_source=d1167fc706d8bb4a356a82d19d9d3304)

---
# 1. Git 是什么？
1. 分布式版本控制工具

# 2. Git 安装
1. Git 定位
2. Git 版本查看 `git -v`
3. Git 资料：
4. Git 互动学习：[404 Not Found](https://oschina.gitee.io/learn-git-branching.)
# 3. Git 配置用户信息
1. 配置用户信息和邮箱
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240309160809.png)
2. 检查用户信息
`git config --list`
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240309161023.png)

3. 清屏 `clear`

# 4. 初始化本地仓库
1. 创建文件夹（表示一个项目）
2. `git init` ——初始化一个本地仓库

# 5. Git 工作流
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240309161914.png)

1. 查看—— `git status`
2. *红色是未跟踪的文件*
3. `git add` ——实现文件的跟踪，加入暂存区
	1. `git add *` / `git add .` ——跟踪全部文件
	2. **自动补全**—— `tab键` 
4. `git commit -m "提交信息"` ——提交版本信息
5. `git log` ——查看版本信息（**黄色**）
6. **`git log --online` ——版本信息简短，呈单行显示**
# 6. 修改文件
Modified

# 7. 删除文件
1. `delete`
2. `rm <file name>` ——删除某个文件
3. Delete
4. Git add . ——git commit -m "工作区"
5. Git rm <>
6. Git rm -f <>


# 8. 撤销本地文件的修改
1. `git restore` ——撤销本地修改（<font color="#ffff00">把文件从暂存区复制到工作区，用来修复本地修改</font>）
2. `git checkout -- file` —— `git restore`
3. ![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240309170854.png)
4. `git switch` ——切换分支
5. `git restore` ——恢复暂存区文件到工作区
# 9. 取消暂存
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310095440.png)

- `git restore --staged file` ——回复暂存区，将内容从本地仓库恢复到暂存区
- `git reset -- file name` ——取消暂存,

# 10. 跳过暂存区
`git commit -a -m "提交信息"`
![image.png|500](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310101915.png)

未被跟踪的文件不能跳过暂存区直接提交！

`git checkout HEAD -- file`


# 11. 版本回退
`git reset 版本号` ——直接回退到后个版本（暂存区）
`git checkout 版本号` ——把暂存区的代码覆盖掉工作区
不适用版本号，默认指向 HEAD 版本
HEAD——当前版本

![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310110729.png)

# 12. 撤销提交
`git reflog` ——清晰看版本


# 13. 设置忽略文件

一些项目不希望 Git 进行管理跟踪，也不希望出现现在未跟踪列表
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310111931.png)
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310112432.png)

![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310112738.png)

<div class="rich-link-card-container"><a class="rich-link-card" href="https://blog.csdn.net/ThinkWon/article/details/101447866" target="_blank">
	<div class="rich-link-image-container">
		<div class="rich-link-image" style="background-image: url('https://g.csdnimg.cn/static/logo/favicon32.ico')">
	</div>
	</div>
	<div class="rich-link-card-text">
		<h1 class="rich-link-card-title">Git 忽略文件. Gitignore 详解_java gitignore log-CSDN 博客</h1>
		<p class="rich-link-card-description">
		文章浏览阅读 7.3 w 次，点赞 97 次，收藏 232 次。在工程中，并不是所有文件都需要保存到版本库中的，例如“target”目录及目录下的文件就可以忽略。在 Git 工作区的根目录下创建一个特殊的. Gitignore 文件，然后把要忽略的文件名填进去，Git 就会自动忽略这些文件或目录。Git 忽略规则优先级在 .gitingore 文件中，每一行指定一个忽略规则，Git 检查忽略规则的时候有多个来源，它的优先级如下（由高到低）：从命令行中读取可用的忽略..._java gitignore log
		</p>
		<p class="rich-link-href">
		https://blog.csdn.net/ThinkWon/article/details/101447866
		</p>
	</div>
</a></div>

)
# 14. 比较文件差异
`git diff` ——比较文件或版本之间的差异（工作区和暂存区）
`git diff --cached` ——（暂存区和本地仓库）




# 15. 创建远程仓库 
1. Gitee （创建远程仓库）
2. 每个仓库都有自己代码协议（`https` ` ssh ` ）
3. **本地仓库和远程仓库关联**—— `git remote add origin ~`（origin 是远程仓库的别名）
4. ![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310171700.png)
5. `git remote` ——**查看远程仓库**
6. *config*——可以查看远程仓库
7. **删除远程仓库**—— `git remote rm origin`

# 16. 本地仓库推送到远程仓库（push）
1.  `git push 别名 本地仓库分支`
2. ![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310172537.png)
# 17. 克隆仓库（克隆远程仓库）
**克隆下来的仓库，默认和远程仓库已经关联好了，不需要再关联**


# 18. 拉取代码（pull）
`git pull origin master`
![image.png|700](https://fig-1321973591.cos.ap-nanjing.myqcloud.com/20240310174219.png)

# 19. 抓取代码
`git fetch` ————只能拉取，不能合并
`git merge` ——手动合并

# 20. 合并冲突
**同一个文件，同一行代码不一样**
**修改旺财的代码，推送到远程仓库**


# 21. 分支
`git branch` ——查看分支
`git branch 分支` ——还在原来你分支（分支创建）
`git checkout 分支` ——切换分支 
`git checkout -b test` ——创建并切换分支
`git checkout -d test` ——删除分支（当前分支删除不了，只能删除其他分支）

# 22. 合并分支冲突




