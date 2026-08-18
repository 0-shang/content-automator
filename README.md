# Content Automator (灵感发散引擎)

[English](#english) | [中文](#中文)

---

## 中文

### 这是什么工具？
Content Automator 是一套基于 Telegram 的全自动化内容生产线。它将您的手机化作超级控制台，抛弃臃肿的网页后台，实现从“信息获取 - 深度阅读 - AI 创作 - 自动排版 - 一键发布”的极致丝滑工作流，帮助您告别内容焦虑，将碎片知识转化为实际产出。

### 核心特色
- **Telegram 即终端**：全流程在 Telegram 内完成，手机即可掌控全局，无需在不同 App 间来回切换。
- **唤醒沉睡知识库**：自动扫描本地 Obsidian 知识库中的未读收藏，AI 提炼精华并直接转化为推文或公众号草稿。
- **智能新闻源聚合**：支持定制专属 RSS 资讯源，每日定时为您抓取全网资讯并批量生成对应的推文矩阵或文章。
- **化碎片灵感为专业爆款**：发送一句简单的灵感或吐槽，AI 会根据你的指令自动发散扩写，生成高质量的专业内容。
- **一键多平台分发**：内容产出后，只需在 Telegram 中点击确认，即可一键发布至 Twitter，或同步存入微信公众号草稿箱。

### 怎么安装？

**环境准备**：请确保您的电脑已经安装了 [Node.js](https://nodejs.org/)（建议版本 18+）。

**1. 定位并创建目录**
在您的 Obsidian 知识库根目录下，打开终端（命令行）运行：
```bash
mkdir content-automator
cd content-automator
```
*(注：放在 Obsidian 根目录是为了方便工具读取您的笔记。如果您不需要处理本地笔记，也可以放在任意目录)*

**2. 初始化项目**
运行以下命令初始化 Agent：
```bash
npx content-automator init
```
*(执行完毕后，当前目录下会自动生成一个 `.env` 配置文件)*

**3. 获取并配置 API 密钥**
用文本编辑器打开生成的 `.env` 文件，按需填入以下关键信息：
- **Telegram 配置**（必须）：
  - `TELEGRAM_BOT_TOKEN`：在 Telegram 中搜索并添加 `@BotFather`，发送 `/newbot` 创建一个机器人，复制获取到的 Token。
  - `TELEGRAM_USER_ID`：在 Telegram 中搜索 `@userinfobot` 或 `@getmyid_bot`，获取您的纯数字 ID。
- **大模型配置**（必须选其一）：
  - 填入 `DEEPSEEK_API_KEY` 或 `GEMINI_API_KEY`。
- **多平台凭证**（可选）：若需使用推特一键发布等高级功能，可填入对应的 Twitter API 凭证。

**4. 启动后台服务**
配置完成后，在终端运行：
```bash
npx content-automator bot
```
看到服务启动成功的提示后，即可在 Telegram 中找到您刚才创建的机器人，发送 `/start` 即可开始体验！

---

## English

### What is this tool?
Content Automator is a fully-automated content production pipeline based on Telegram. It turns your Telegram client into a super-console, achieving a seamless workflow from "Information Intake -> Deep Reading -> AI Generation -> Auto-formatting -> One-Click Publishing", helping you transform scattered knowledge into actual output.

### Core Features
- **Telegram as the Ultimate Console**: Manage your entire content pipeline directly from Telegram on your phone.
- **Revive Your Knowledge Base**: Automatically fetches and summarizes unread articles from your Obsidian vault, converting them into publish-ready drafts.
- **Intelligent News Curation**: Define your customized RSS feeds. The bot aggregates news daily and batch-generates related tweets or articles.
- **Turn Fragments into Professional Posts**: Send a casual thought, and the bot will auto-expand it into a highly-engaging Twitter/X draft.
- **Frictionless Multi-Platform Distribution**: Review AI-generated drafts in Telegram and push them instantly to Twitter or sync to your WeChat Official Account.

### How to Install?

**Prerequisites**: Please ensure you have [Node.js](https://nodejs.org/) installed (version 18+ recommended).

**1. Create Working Directory**
Open a terminal in your Obsidian vault root directory and run:
```bash
mkdir content-automator
cd content-automator
```
*(Note: Placing it in the Obsidian root allows the tool to read your notes. If you don't need local notes processing, any directory works.)*

**2. Initialize the Project**
Run the following command to initialize the agent:
```bash
npx content-automator init
```
*(This will automatically generate a `.env` configuration file in the current directory.)*

**3. Configure API Keys (.env)**
Open the generated `.env` file in any text editor and fill in the required info:
- **Telegram Setup** (Required):
  - `TELEGRAM_BOT_TOKEN`: Search for `@BotFather` in Telegram, send `/newbot` to create a bot, and copy the provided token.
  - `TELEGRAM_USER_ID`: Search for `@userinfobot` in Telegram to get your personal numerical ID.
- **LLM Setup** (Choose One):
  - Provide either `DEEPSEEK_API_KEY` or `GEMINI_API_KEY`.
- **Publishing Credentials** (Optional): Provide Twitter API keys if you wish to use the one-click publishing feature.

**4. Launch the Service**
Once configured, run:
```bash
npx content-automator bot
```
After a successful startup, open Telegram, find the bot you just created, send `/start`, and begin your automated content creation journey!
