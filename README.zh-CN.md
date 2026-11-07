# Repo Shopping Cards

[English](README.md) | **简体中文**

像网购一样浏览 GitHub 仓库：先扫一眼精简卡片，感兴趣再展开详情，然后选择 **深入分析**、打开 **GitHub**，或 **对比仓库**。

这是一套 ChatGPT 指令包，复制粘贴即可使用，无需 MCP、API Key、浏览器扩展或构建步骤。

## 快速开始

1. 复制 [`instructions/project.md`](instructions/project.md) 的全部内容。
2. 在 [ChatGPT](https://chatgpt.com) 中创建或打开一个 **Project**，进入项目指令设置（不同客户端名称可能不同）。
3. 粘贴并保存。如有想保留的原有指令，请合并后再保存。
4. 在该 Project **内部**新建对话，例如：

   > 帮我找 3 个适合学习 AI Agent 架构的 GitHub 项目。

请粘贴到指令输入框，而不是把文件作为资料上传。

## 兼容性

| 客户端 | 普通对话 | Project 内对话 |
| --- | :---: | :---: |
| 网页版 | ✅ | ✅ |
| iOS App | ✅ | ✅ |
| 桌面版，ChatGPT 模式 | ✅ | ❌ |
| 桌面版，Codex 模式 | ❌ | ❌ |

在桌面版中，请使用 ChatGPT 模式下的普通对话，并在对话开头粘贴指令。

## 其他使用方式

- **单次对话：** 在对话开头粘贴 `project.md`，适合快速试用。每开一个新对话需重新粘贴。
- **全局自定义指令**（[`instructions/global.md`](instructions/global.md)）：未经测试，不推荐。规则可能影响无关的对话。

## 卡片说明

- 每行一张卡片，所有屏幕尺寸下均纵向排列。
- 卡片包含项目名称、准确的 `owner/repo`、一句话简介和技术标签。Star、许可证和活跃度仅在核实后显示。
- **查看详情** 展开五项简短说明：是什么、解决什么问题、怎么解决、适用场景、技术思路。同一时间只展开一张卡片。
- **深入分析** 围绕你的目标，基于源码进行深度分析。
- **GitHub** 打开该仓库。
- **对比仓库** 在列表下方只出现一次，对比当前显示的所有仓库。
- 语言跟随对话。如需切换，请明确说明。

浏览卡片不会自动触发分析或对比。不支持原生卡片的客户端会退回为精简的 Markdown 列表。

## 预览设计

用现代浏览器打开 [`ui-demo.html`](ui-demo.html)。它是独立文件，使用示例数据，不会发送任何内容。你可以切换 English / 中文、展开详情，并把“深入分析”或“对比”提示词复制到 ChatGPT 中。

## 常见问题

- **卡片没有出现：** 确认你在正确的 Project 或对话中，并使用[受支持的客户端](#兼容性)。
- **卡片并排显示：** 要求“每行一张卡片”，或重新安装最新指令。
- **语言不对：** 明确说明想要的语言。
- **信息有误：** 要求核实来源，并省略未经验证的内容。
- **更新或移除：** 直接在 ChatGPT 中修改指令。更新本仓库不会自动更改你的 ChatGPT 设置。

## 文件结构

```
repo-cards/
├── README.md
├── README.zh-CN.md
├── instructions/
│   ├── project.md
│   └── global.md
└── ui-demo.html
```

V1 暂不包含：身份认证、私有仓库、收藏、筛选和后台任务。

OpenAI 文档：[Project 指令](https://learn.chatgpt.com/docs/projects) · [自定义指令](https://learn.chatgpt.com/docs/personalize)
