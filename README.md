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
1. **定位 Obsidian 知识库**：在您的 Obsidian 知识库根目录下，打开终端运行：
   ```bash
   mkdir content-automator
   cd content-automator
   ```
2. **初始化配置**：运行以下命令初始化项目（开发者也可选择直接 `git clone` 源码）：
   ```bash
   npx content-automator init
   ```
3. **配置 API 密钥**：打开项目目录中生成的 `.env` 文件，填入各项必要的 API 密钥（如 Telegram Bot Token、您的 Telegram ID、大模型 DeepSeek/Gemini 的 API Key、Twitter 凭证等）。
4. **启动服务**：
   ```bash
   npx content-automator bot
   ```
   看到成功提示后，服务即在后台运行。打开 Telegram 找到您的机器人，发送 `/start` 即可开始体验！

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
1. **Create Directory**: Open a terminal in your Obsidian vault root directory and run:
   ```bash
   mkdir content-automator
   cd content-automator
   ```
2. **Initialize**: Run the following command to initialize the agent:
   ```bash
   npx content-automator init
   ```
3. **Configure APIs (.env)**: Open the generated `.env` file and fill in the required API keys (Telegram Token, AI keys like DeepSeek/Gemini, Twitter API keys, etc.).
4. **Launch the Service**:
   ```bash
   npx content-automator bot
   ```
   Once started, open Telegram, find your bot, send `/start`, and begin your automated content creation journey!
