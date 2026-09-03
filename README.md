<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=25&duration=3400&pause=800&color=4ADE80&center=true&vCenter=true&width=680&height=70&lines=%24+whoami+%3E%3E+Yht20927;%24+mission+%3E%3E+real+browsers%2C+not+simulation;%24+stack+%3E%3E+JS+%2B+TS+%2B+Python+%2B+Node" alt="Yht20927 — terminal intro" />
</p>

<p align="center">
  🛠️ 用 <b>真实浏览器 + LLM</b> 构建可靠的 AI CLI 工具 —— 社媒自动化 · AI 视频管线 · Agent 记忆
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Total%20Stars-144%2B-22c55e?style=flat-square&logo=github&logoColor=white&labelColor=0d1117" alt="Total Stars"/>
  <img src="https://img.shields.io/badge/Public%20Repos-9-22c55e?style=flat-square&logo=github&logoColor=white&labelColor=0d1117" alt="Public Repos"/>
  <img src="https://img.shields.io/badge/Followers-8-22c55e?style=flat-square&logo=github&logoColor=white&labelColor=0d1117" alt="Followers"/>
</p>

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Yht20927&show_icons=true&count_private=true&hide_border=true&rank_icon=github&title_color=4ade80&icon_color=4ade80&text_color=cbd5e1&bg_color=0d1117&border_radius=14" alt="GitHub Stats" height="170"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Yht20927&layout=compact&hide_border=true&langs_count=6&title_color=4ade80&text_color=cbd5e1&bg_color=0d1117&border_radius=14" alt="Top Languages" height="170"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Yht20927&hide_border=true&background=0D1117&stroke=30363D&ring=4ADE80&fire=4ADE80&currStreakNum=4ADE80&currStreakLabel=cbd5e1&sideNums=cbd5e1&sideLabels=cbd5e1&dates=8b949e" alt="GitHub Streak" height="150"/>
</p>

---

## 🧭 About

别人用「模拟请求」对抗平台,我用 **油猴脚本 + Bridge Server 驱动真实浏览器** —— 在风控 / 反爬环境里也能稳定操作,再交给 **LLM** 做决策与拟人化,让每个工具「会思考」而不是「照着跑」。

**Bridge Framework** 统一架构,已在 5 个平台落地:

```
[浏览器] 油猴脚本:采集页面数据 / 执行真实操作
    │ JSON 双向通信
    ▼
[本地]   Bridge Server:通信、状态管理
    │ JSON 双向通信
    ▼
[CLI]    AI Agent:命令执行 / LLM 决策 / 拟人化回复
```

社媒自动化之外,我还在做 **AI 视频管线**(一句话想法 → 口播稿 → TTS 配音 → whisper 对齐 → 富视觉渲染)和 **Agent 记忆基础设施** —— 目标是让 AI 既能操作真实世界,也能生产高质量内容、长期记忆。

## 🧰 Tech Stack

<div align="center">
  <img src="https://skillicons.dev/icons?i=js,ts,python,nodejs,bash,git,github" alt="Tech Stack"/>
</div>

**核心能力:**
- 🔐 **真实浏览器自动化** — 油猴脚本 + Bridge Server,反检测 / 风控环境稳定运行
- 🕵️ **拟人化风控守卫** — 人格化回复 + 行为模拟 + 随机延迟,降低账号限流风险
- 🧠 **AI Agent 集成** — LLM 决策、智能匹配、人格化回复,让工具会「思考」
- 📊 **数据采集** — 全量评论爬取、嵌套回复、直播 ASR 转写
- 🎬 **AI 视频管线** — 音频先行 + TTS + 对齐 + 富视觉渲染(ttsVoice / HyperFrames)
- 🗂️ **Agent 记忆系统** — 分层记忆,跨会话 / 跨项目 / 跨机器持久化

## 📦 Featured Projects

### 🤖 Bridge Framework · 社媒自动化

| 项目 | 说明 | ⭐ |
|---|---|---|
| [🎵 **douyin-cli**](https://github.com/Yht20927/douyin-cli) | 抖音全自动评论管理:搜索、全量评论爬取(含嵌套回复)、AI 智能回复、运营仪表盘 | 52 |
| [📕 **xiaohongshu-cli**](https://github.com/Yht20927/xiaohongshu-cli) | 小红书全自动管理:搜索、评论爬取(含嵌套回复)、AI 智能回复、运营仪表盘 | 28 |
| [💼 **BossZhipin-cli**](https://github.com/Yht20927/BossZhipin-cli) | BOSS直聘命令行工具:Bridge Server + 油猴脚本驱动真实浏览器,搜索职位 / 智能匹配评分 / 批量打招呼 / LLM 招呼语 / @ref 缓存,17 条命令 | 13 |
| [🎬 **tiktok-cli**](https://github.com/Yht20927/tiktok-cli) | 基于 Bridge Framework 的 TikTok 全自动评论管理:搜索、全量评论爬取(含嵌套回复)、AI 智能回复与运营 | 2 |
| [📈 **ths-cli**](https://github.com/Yht20927/ths-cli) | 基于 Bridge Framework 的同花顺工具,提供基本数据服务与简易量化 | 5 |

### 🎬 媒体与创作

| 项目 | 说明 | ⭐ |
|---|---|---|
| [🎥 **douyin-living**](https://github.com/Yht20927/douyin-living) | 抖音直播全自动录制 + 多模态 AI 智能切片:录制、弹幕、ASR、信号融合、自动剪辑高光片段 | 33 |

### 🧠 AI Agent 基础设施

| 项目 | 说明 | ⭐ |
|---|---|---|
| [🧠 **my-claude-memory**](https://github.com/Yht20927/my-claude-memory) | 为 Claude Code 等 Agent 打造的分层记忆管理系统,让 AI 跨会话 / 跨项目 / 跨机器持久化并共享项目与个人知识 | 4 |

### 🔧 效率工具

| 项目 | 说明 | ⭐ |
|---|---|---|
| [📝 **markdown-to**](https://github.com/Yht20927/markdown-to) | md-to.com 核心功能的命令行复刻,所有转换本地完成,支持批量与脚本集成 | 3 |

## 🔭 正在做

- 🎬 **AI 视频管线** — 一句话想法 → 口播稿 → 整篇 TTS 配音 → whisper 对齐 → 富视觉渲染,产出「非网页风」成片(ttsVoice + HyperFrames)
- 🤖 **boss-cli 迭代** — 打磨 BOSS直聘 17 条命令的智能招聘助手

## 📫 Contact

- GitHub: [@Yht20927](https://github.com/Yht20927)

> 🌱 持续迭代中 —— 欢迎 star、issue 和 PR,一起让浏览器自动化更可靠。

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=Yht20927&color=22c55e&style=flat-square" alt="Profile views"/>
</p>
