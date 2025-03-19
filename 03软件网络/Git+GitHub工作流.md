# 1. 引言 
Git 版本控制“版本”、“文件名”、“修改时间”、“修改内容”
分布式版本控制软件 

## Git 流程 
1. 本地建立文件夹（`git init`) 建立 Git 仓库
2. 建立文件（abc. Txt）
3. `git add abc.txt ` (把指定文件（abc. Txt）代码提交暂存区)
4. `git add .` (把所有文件提交到暂存区)
5. `git commit` (提交到仓库)、`git commit -m "备注信息"`
6. `git log` (查看节点)
	1. `git log --stat`（查看具体修改内容、关注 `commit`）
	2. `git diff [commit ID]`
	3. `git reset --hard [commit id]` （将代码回退到指定的节点）
	4. `git checkout [commit id]`将代码回退到指定的节点
7. Git 完成提交的三个内容：==修改文件内容、Git add、Git commit==
8. Git 可视化工具 
9. `git branch` 
10. `git checkout -b 分支`
11. 

