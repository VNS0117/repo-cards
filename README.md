# Repo Shopping Cards

Browse GitHub repositories like shopping: scan compact cards, open details when interested, then choose **Analyze**, **GitHub**, or **Compare repositories**.

**V1 is a ChatGPT instruction pack.** Copy the instructions into ChatGPT to use it. No MCP, React, API key, extension, installation command, or build step is required. Native cards and controls depend on the client; concise Markdown is the fallback.

## Install in a ChatGPT Project — recommended

1. Open [instructions/project.md](instructions/project.md) and copy the **entire file contents**.
2. Create or open a Project in [ChatGPT](https://chatgpt.com).
3. Open the Project menu/settings and find its instructions; labels may vary by client.
4. Paste and save the rules. Merge with any existing instructions you want to keep.
5. Start a chat **inside that Project**, for example:

   > Find three GitHub repositories to learn Agent orchestration.

The instructions apply across that Project's chats. Uploading the Markdown file as a source is different from pasting it into the instructions field.

中文：复制 [Project 指令](instructions/project.md) 全文 → 创建或打开 ChatGPT Project → 项目菜单或设置中的指令 → 粘贴并保存 → 在该 Project 中提问：**“帮我找 3 个适合学习 AI Agent 架构的 GitHub 项目。”**

## Other ways to use it

- **Global Custom Instructions:** Copy [instructions/global.md](instructions/global.md) into ChatGPT's personalization/custom-instructions settings. Merge it with existing preferences within the available character limit. It uses a conservative trigger for discovery or comparison of two or more GitHub repositories. Use Project instructions for project-specific behavior.
- **Single chat:** Paste [instructions/project.md](instructions/project.md) into a fresh chat, then ask to explore repositories. Paste it again when starting a different chat.

Project installation keeps these rules within one Project. Global instructions can influence ordinary chats; the conservative trigger reduces interference with unrelated requests. A single-chat prompt is a quick trial without changing settings.

## How cards work

**Always one card per row**, stacked vertically on desktop, tablet, and mobile. Cards never appear side by side. The Markdown fallback also uses one repository block after another.

Each card includes the project name and exact `owner/repo`, a one-line value proposition, supported technology tags, and verified metadata when available. Missing or unverified stars, licenses, and activity are omitted. Displayed changing metrics need source/freshness context; custom or restrictive licenses must be identified accurately.

- **View details / 查看详情** reveals five short answers: what it is, the problem, the solution, practical use cases, and the technical approach. Details start collapsed when supported; opening another card closes the previous one.
- **Analyze / 深入分析** requests a source-based deep dive into that repository for your goal.
- **GitHub** opens the repository. Its label is always exactly `GitHub`.
- **Compare repositories / 对比仓库** appears once below the collection and targets all currently displayed repositories for your goal.

Descriptions, generic labels, headings, and prompts follow the conversation language. Explicit language requests take priority; project names and technical terms such as Python, Agent, and RAG stay intact.

Browsing cards does not automatically run deep analysis or comparison. Where local disclosure controls are available, expansion only reveals prepared details. On a text-only client, details require a follow-up message; suggested Analyze/Compare prompts remain usable. Native formatting is best-effort.

## Preview the design

Open [ui-demo.html](ui-demo.html) in a modern browser. This standalone file needs no server or build. GitHub links open external pages when chosen.

1. Browse the three sample cards, **one per row**, with details initially collapsed.
2. Switch **English / 中文** to inspect localized cards and prompts. The initial language follows the browser preference.
3. Open details, then another card's details to see the single-open behavior.
4. Choose Analyze on one card, or Compare below the collection, to preview a follow-up prompt.
5. Copy the prompt into ChatGPT when you want to continue. If copying is unavailable, select and copy it manually. Close the dialog or press Escape to return.

The demo uses illustrative summaries and a **general exploration / 一般探索** goal. Unverified stars, licenses, and activity are hidden. It makes no repository retrieval or analysis requests and sends no messages. The installed instructions use your actual goal and available sources instead. Opening or uploading the HTML does not install a native ChatGPT component.

## Update, remove, and troubleshoot

- **Update:** Replace or merge the installed rules with the current instruction file. Downloading an updated repository does not change ChatGPT settings automatically.
- **Remove:** Delete these rules from Project/Global settings, or start a chat without the single-chat prompt.
- **Cards do not appear:** Check that you are using the intended Project or chat. Native controls vary by client, model, and context; a compact vertical Markdown list is an acceptable fallback.
- **Cards appear side by side:** Ask for one card per row and reinstall the current instructions. They explicitly request a single vertical column at every screen size.
- **Wrong language:** State the desired language explicitly.
- **Wrong metadata:** Ask for source verification and omission of unverified values.
- **Wrong comparison targets:** State the current repository set. The instructions ask for clarification when targets are ambiguous.

## Package contents

```text
repo-cards/
├── .gitignore
├── README.md
├── instructions/
│   ├── project.md
│   └── global.md
└── ui-demo.html
```

The instructions work for AI and non-AI repositories. Authentication, private-repository access, favorites, multiselect, filters, and background jobs are outside V1.

OpenAI documents how [Project instructions apply across project chats](https://learn.chatgpt.com/docs/projects) and how [custom instructions carry preferences across chats](https://learn.chatgpt.com/docs/personalize).
