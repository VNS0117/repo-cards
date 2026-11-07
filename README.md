# Repo Shopping Cards

**English** | [简体中文](README.zh-CN.md)

Browse GitHub repositories like online shopping: scan compact cards, expand for details, then **Analyze**, open on **GitHub**, or **Compare repositories**.

This is a ChatGPT instruction pack. Copy, paste, done. No MCP, API key, extension, or build step.

## Quick start

1. Copy the entire contents of [`instructions/project.md`](instructions/project.md).
2. In [ChatGPT](https://chatgpt.com), create or open a **Project** and open its instructions (the label varies by client).
3. Paste and save. Merge with any existing instructions you want to keep.
4. Start a chat **inside that Project**, for example:

   > Find three GitHub repositories to learn Agent orchestration.

Paste into the instructions field. Uploading the file as a source is not the same thing.

## Compatibility

| Client | Normal chat | Project chat |
| --- | :---: | :---: |
| Web | ✅ | ✅ |
| iOS app | ✅ | ✅ |
| Desktop app, ChatGPT mode | ✅ | ❌ |
| Desktop app, Codex mode | ❌ | ❌ |

On the desktop app, use a normal chat in ChatGPT mode and paste the instructions at the start of the chat.

## Other ways to use it

- **Single chat:** paste `project.md` at the start of a chat for a quick trial. Repeat for each new chat.
- **Global custom instructions** ([`instructions/global.md`](instructions/global.md)): untested, and not recommended. The rules may apply to unrelated conversations.

## How cards work

- One card per row, stacked vertically on every screen size.
- Each card shows the project name, exact `owner/repo`, a one-line summary, and tech tags. Stars, license, and activity appear only when verified.
- **View details** expands five short answers: what it is, the problem, the solution, use cases, and technical approach. One card is open at a time.
- **Analyze** starts a source-based deep dive for your goal.
- **GitHub** opens the repository.
- **Compare repositories** appears once below the list and covers every displayed repo.
- Language follows the conversation. Ask explicitly to switch.

Browsing never triggers analysis or comparison on its own. Clients without native cards fall back to a compact Markdown list.

## Preview the design

Open [`ui-demo.html`](ui-demo.html) in a modern browser. It is standalone, uses sample data, and sends nothing. Switch between English and 中文, expand details, and copy the Analyze or Compare prompt into ChatGPT.

## Troubleshooting

- **Cards don't appear:** confirm you are in the right Project or chat and on a [supported client](#compatibility).
- **Cards sit side by side:** ask for one card per row, or reinstall the latest instructions.
- **Wrong language:** state the language you want.
- **Wrong metadata:** ask for source verification and to omit unverified values.
- **Update or remove:** edit the instructions in ChatGPT. Updating this repo does not change your ChatGPT settings.

## Files

```
repo-cards/
├── README.md
├── README.zh-CN.md
├── instructions/
│   ├── project.md
│   └── global.md
└── ui-demo.html
```

Out of scope for V1: authentication, private repositories, favorites, filters, and background jobs.

OpenAI docs: [Project instructions](https://learn.chatgpt.com/docs/projects) · [Custom instructions](https://learn.chatgpt.com/docs/personalize)
