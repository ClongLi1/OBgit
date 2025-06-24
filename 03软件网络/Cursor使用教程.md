---
tags:
  - Cursor
  - 教程
---
# Cursor IDE 使用教程

  

## 目录

- [简介](#简介)

- [安装与配置](#安装与配置)

- [界面概览](#界面概览)

- [基础功能](#基础功能)

- [AI 辅助功能](#ai-辅助功能)

- [快捷键](#快捷键)

- [高级特性](#高级特性)

- [常见问题](#常见问题)

  

## 简介

  

Cursor 是一款基于 VS Code 的现代化智能编程编辑器，集成了强大的 AI 辅助功能。它不仅保留了 VS Code 的所有优秀特性，还加入了 AI 驱动的代码补全、重构和调试功能，让编程更加高效。

  

## 安装与配置

  

### 系统要求

- Windows 10/11

- macOS 10.15+

- Linux (Ubuntu 18.04+)

- 至少 4GB RAM

- 稳定的网络连接（用于 AI 功能）

  

### 安装步骤

1. 访问 [Cursor 官网](https://cursor.sh)

2. 下载对应操作系统的安装包

3. 运行安装程序

4. 首次启动时登录或注册账号

  

### 基础配置

1. 选择主题（File > Preferences > Color Theme）

2. 配置字体（File > Preferences > Settings > Font）

3. 设置 AI 模型（File > Preferences > AI Settings）

  

## 界面概览

  

### 主要组件

- 活动栏（左侧）：文件浏览器、搜索、Git 等

- 编辑区（中央）：代码编辑主区域

- 状态栏（底部）：Git 状态、编码、行号等

- 终端（底部）：集成终端

- AI 聊天面板（右侧）：与 AI 助手交互

  

### 布局调整

- 使用 `Ctrl+B` 切换侧边栏

- 使用 `Ctrl+J` 切换终端

- 使用 `Ctrl+Shift+P` 打开命令面板

  

## 基础功能

  

### 文件操作

- 新建文件：`Ctrl+N`

- 打开文件：`Ctrl+O`

- 保存文件：`Ctrl+S`

- 关闭文件：`Ctrl+W`

  

### 编辑功能

- 多光标编辑：`Alt+Click` 或 `Ctrl+Alt+↑/↓`

- 行操作：

  - 复制行：`Ctrl+C`（无选中）

  - 移动行：`Alt+↑/↓`

  - 删除行：`Ctrl+Shift+K`

- 代码折叠：`Ctrl+Shift+[` 或 `Ctrl+Shift+]`

  

### 搜索与替换

- 文件内搜索：`Ctrl+F`

- 全局搜索：`Ctrl+Shift+F`

- 替换：`Ctrl+H`

- 转到定义：`F12`

- 查找引用：`Shift+F12`

  

## AI 辅助功能

  

### AI 聊天

- 打开 AI 聊天：`Ctrl+K` 或 `Ctrl+L`

- 常用命令：

  - `/edit` - 编辑当前代码

  - `/explain` - 解释选中的代码

  - `/test` - 生成测试用例

  - `/doc` - 生成文档注释

  

### 代码生成

- 使用 `Ctrl+K` 触发 AI 补全

- 在注释中描述需求，AI 会生成相应代码

- 支持多种编程语言的代码生成

  

### 代码重构

- 使用 AI 优化代码结构

- 自动修复代码问题

- 智能变量重命名

  

## 快捷键

  

### 通用快捷键

| 功能 | Windows/Linux | macOS |

|------|--------------|-------|

| 命令面板 | `Ctrl+Shift+P` | `Cmd+Shift+P` |

| 快速打开 | `Ctrl+P` | `Cmd+P` |

| 保存 | `Ctrl+S` | `Cmd+S` |

| 撤销 | `Ctrl+Z` | `Cmd+Z` |

| 重做 | `Ctrl+Y` | `Cmd+Y` |

  

### AI 相关快捷键

| 功能 | Windows/Linux | macOS |

|------|--------------|-------|

| AI 聊天 | `Ctrl+K` | `Cmd+K` |

| 代码补全 | `Ctrl+Space` | `Cmd+Space` |

| 解释代码 | `Ctrl+Shift+L` | `Cmd+Shift+L` |

  

## 高级特性

  

### Git 集成

- 内置 Git 支持

- 可视化分支管理

- 提交历史查看

- 冲突解决工具

  

### 调试功能

- 断点设置：点击行号或 `F9`

- 开始调试：`F5`

- 单步执行：`F10`（步过）或 `F11`（步入）

- 查看变量：调试面板

  

### 扩展支持

- 支持 VS Code 扩展

- 常用扩展推荐：

  - GitLens

  - Prettier

  - ESLint

  - Python

  - Java Extension Pack

  

## 常见问题

  

### 性能优化

1. 关闭不必要的扩展

2. 定期清理工作区

3. 使用 `.gitignore` 排除大文件

4. 调整 AI 模型设置

  

### 故障排除

1. AI 功能无响应

   - 检查网络连接

   - 确认 API 密钥有效

   - 重启 IDE

  

2. 编辑器卡顿

   - 检查内存使用

   - 关闭大型文件

   - 更新到最新版本

  

3. 扩展冲突

   - 逐个禁用扩展排查

   - 更新扩展版本

   - 清理扩展缓存

  

### 最佳实践

1. 定期备份工作

2. 使用版本控制

3. 保持 IDE 更新

4. 合理使用 AI 功能

5. 遵循代码规范

  

## 资源链接

- [官方文档](https://cursor.sh/docs)

- [GitHub 仓库](https://github.com/getcursor/cursor)

- [社区论坛](https://community.cursor.sh)

- [问题反馈](https://github.com/getcursor/cursor/issues)

  

---

  

*注：本教程会随 Cursor 版本更新而更新，请以最新版本为准。*