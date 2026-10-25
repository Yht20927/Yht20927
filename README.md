<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/banner.svg" width="100%" alt="YHT20927 / BRIDGE FRAMEWORK banner"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/SIGNAL-213%E2%98%85-f472b6?style=flat&labelColor=0d1117" alt="213 stars"/>
  <img src="https://img.shields.io/badge/FORKS-37-22d3ee?style=flat&labelColor=0d1117" alt="37 forks"/>
  <img src="https://img.shields.io/badge/NODES-10%20repos-a78bfa?style=flat&labelColor=0d1117" alt="10 repos"/>
  <img src="https://img.shields.io/badge/FOLLOWERS-12-4ade80?style=flat&labelColor=0d1117" alt="12 followers"/>
  <img src="https://img.shields.io/badge/COMMITS-206%2B-9ca3c0?style=flat&labelColor=0d1117" alt="206 commits"/>
  <img src="https://komarev.com/ghpvc/?username=Yht20927&color=22d3ee&style=flat&label=VIEWS" alt="views"/>
</p>

> **一个人就是一整套「Bridge Framework」神经中枢。** 别人拿「模拟请求」对抗平台，我用 **油猴脚本 + Bridge Server 驱动真实浏览器**，在风控 / 反爬环境里稳定操作；再交给 **LLM** 做决策与拟人化——让每个工具「会思考」，而不是「照着跑」。
>
> 目前 **10 个仓库**、**5 个平台节点**、**5 个独立 Bridge 端口** 可并行在线：抖音 / 小红书 / BOSS直聘 / TikTok / 同花顺，外加直播切片、AI 视频管线、Agent 记忆与源码安全研究。

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/boot.svg" width="100%" alt="boot sequence"/>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 📡 PATCH NOTES · 最近信号

不是冻结的简历，是仍在持续推送的代码。以下为最近四个节点的真实 commit：

| 时间 | 节点 | 最新变更 |
|---|---|---|
| `2026-10-19` | **ths-cli** | 科创板指数 + 资金流排行解析 + 成交额均值修正 |
| `2026-10-10` | **douyin-cli** | 多账号收尾：账号无关命令忽略 `--account`，新增 `videos` 命令 |
| `2026-08-19` | **tiktok-cli** | v0.3 实战修复：登录检测假阴性、评论缓存陈旧、写超时 |
| `2026-08-03` | **BossZhipin-cli** | 17 条命令稳定版：匹配评分、`@ref` 缓存、48s 写节流 |

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 💻 LIVE SESSION · 实时会话

不是演示视频，是日常：一条命令挂到真实 Chrome 上，剩下的交给 Bridge 与 LLM。

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/terminal.svg" width="100%" alt="live bridge session terminal"/>
</p>

<p align="center">
  <sub><code>attach → crawl → llm reply → video make</code> ：从接管浏览器到产出成片，全链路一条命令。</sub>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 🛰 NODE SCAN · 平台在线矩阵

同一套神经中枢，已在 **5 个平台**落地——每条链路都是真实浏览器 + Bridge 通信 + LLM 决策：

| 节点 | 平台 | 当前能力 | 信号 |
|---|---|---|---|
| 🎵 **douyin-cli** | 抖音 | 搜索 / 全量评论 / 嵌套回复 / **图片评论** / **多账号** / ReplyEngine | `76★ · 17 forks` |
| 📕 **xiaohongshu-cli** | 小红书 | 笔记搜索 / 评论 / 嵌套回复 / 7 人格 AI 回复 / 行为模拟 | `36★ · 4 forks` |
| 💼 **BossZhipin-cli** | BOSS直聘 | 职位搜索 / 匹配评分 / 批量打招呼 / LLM 招呼语 / 17 命令 | `22★ · 8 forks` |
| 📈 **ths-cli** | 同花顺 | 行情 / K线 / 14 项指标 / 选股 / 回测 / 盘中风控 / 组合画像 | `13★ · 1 fork` |
| 🎬 **tiktok-cli** | TikTok | 搜索 / 评论 / 嵌套回复 / 写接口实测 / 长串缓存 | `2★` |

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/radar.svg" width="100%" alt="platform radar & matrix"/>
</p>

## ⚙ ARCHITECTURE · 数据流

```bash
┌──────────────┐   JSON ⇅   ┌────────────────┐   JSON ⇅   ┌──────────────┐
│   BROWSER    │ ◄───────► │  BRIDGE-SERVER  │ ◄───────► │   AI AGENT    │
│  userscript  │            │  state · sync   │            │   llm · brain │
└──────────────┘            └────────────────┘            └──────────────┘
```

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/arch.svg" width="100%" alt="bridge flow diagram"/>
</p>

**为什么是「真实浏览器」而不是「模拟请求」：**

| 维度 | 模拟请求 / 协议逆向 | Bridge Framework |
|---|---|---|
| 运行位置 | 无头进程直接发包 | 真实 Chrome 标签页内 |
| 环境指纹 | 需自行伪造，平台一改就失效 | 与真实用户同一环境，天然一致 |
| 页面改版 | 签名算法一变即全线崩溃 | DOM 层适配，抗改版 |
| 人机验证 | 依赖额外打码通道 | 在浏览器内自然完成 |
| 决策能力 | 流程硬编码 | LLM 实时决策 + 拟人化节奏 |
| 账号态 | 需维护 Cookie / 签名 | 直接复用已登录浏览器会话 |

**Bridge 端口分配**（五个节点可同时在线，互不抢占）：

| 节点 | 端口 | 节点 | 端口 |
|---|:-:|---|:-:|
| `douyin-cli` | `19422` | `xiaohongshu-cli` | `19424` |
| `tiktok-cli` | `19423` | `BossZhipin-cli` | `19425` |
| `ths-cli` | `19429` |  |  |

**最小启动链路**（以 douyin-cli 为例）：

```bash
git clone https://github.com/Yht20927/douyin-cli && cd douyin-cli
npm install && cp config.example.json config.json
node server.js &                 # Bridge Server :19422
# 浏览器安装 scripts/douyin.user.js → 打开 douyin.com 并保持登录
node cli.js status               # totalConnections >= 1 即接通
node cli.js search "AI" --count 5
```

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 🧭 MISSION LOG · 部署时间线

从记忆基础设施到跨平台自动化，节点一个个亮起来：

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/chrono.svg" width="100%" alt="project chronology"/>
</p>

```text
2026.04  毕设 · 源码级恶意代码检测      2026.07  BossZhipin-cli
2026.04  my-claude-memory              2026.08  tiktok-cli
2026.05  markdown-to                   2026.08  ths-cli
2026.06  douyin-cli / douyin-living    2026.08  GitHub Profile
2026.06  xiaohongshu-cli               2026.10  ths-cli 科创板 / 资金流
```

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 🧬 LOADOUT · 武器库

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/skills.svg" width="100%" alt="tech proficiency bars"/>
</p>

**真实浏览器自动化** · 油猴脚本 + Bridge Server，反检测 / 风控环境稳定运行
**拟人化风控守卫** · 人格化回复 + 行为模拟 + 随机延迟 + 写节流 + 断路器
**AI Agent 集成** · LLM 决策、智能匹配、人格化回复，Anthropic / OpenAI 双 Provider
**数据采集** · 全量评论爬取、嵌套回复、直播弹幕 / ASR 转写、SQLite 持久化
**AI 视频管线** · 音频先行 + TTS + whisper 对齐 + 富视觉渲染
**Agent 记忆系统** · L1-L4 分层记忆，跨会话 / 跨项目 / 跨机器持久化
**安全研究** · UniXcoder + Graph-RAG + LoRA，源码级恶意代码语句定位
**工程化** · Node.js / Python / Bash / SQLite / ffmpeg / faster-whisper / Playwright

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 🎬 AI VIDEO PIPELINE · 从想法到成片

社媒自动化之外，我还在做 **AI 视频管线**（一句话想法 → 口播稿 → TTS 配音 → whisper 对齐 → 富视觉渲染）和 **Agent 记忆基础设施**——目标是让 AI 既能操作真实世界，也能生产高质量内容、长期记忆。

| 阶段 | 输入 | 产出 |
|---|---|---|
| 1. 选题 | 一句话想法 / 大纲 | 结构化的视频脚本 |
| 2. 口播 | 脚本 | 分镜节奏 + 口播稿 |
| 3. 配音 | 口播稿 | 整篇 TTS 音轨 |
| 4. 对齐 | 音轨 + 文本 | whisper 时间轴 / 字幕 |
| 5. 视觉 | 时间轴 | 非网页风的富视觉动画 |
| 6. 成片 | 全部素材 | `4k.mp4` |

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/pipeline.svg" width="100%" alt="ai video pipeline"/>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 📡 LIVE TELEMETRY · 实时遥测

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Yht20927&show_icons=true&count_private=true&hide_border=true&rank_icon=github&title_color=f472b6&icon_color=22d3ee&text_color=cbd5e1&bg_color=0d1117&border_radius=14" alt="GitHub Stats" height="170"/>
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Yht20927&layout=compact&hide_border=true&langs_count=6&title_color=22d3ee&text_color=cbd5e1&bg_color=0d1117&border_radius=14" alt="Top Languages" height="170"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Yht20927&bg_color=0d1117&color=9ca3c0&line=f472b6&point=22d3ee&area=true&area_color=250b2e&hide_border=true&border_radius=14&custom_title=Contribution%20Signal" alt="Activity Graph" width="100%"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Yht20927&hide_border=true&background=0D1117&stroke=30363D&ring=F472B6&fire=22D3EE&currStreakNum=F472B6&currStreakLabel=22D3EE&sideNums=cbd5e1&sideLabels=64748b&dates=64748b" alt="GitHub Streak" height="150"/>
</p>

<details>
<summary><b>🏆 TROPHIES — 成就墙</b>（点击展开）</summary>
<br/>
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=Yht20927&theme=radical&no-frame=true&no-bg=true&column=4&margin-w=10" alt="Trophies" width="100%"/>
</p>
</details>

<details>
<summary><b>🐍 SNAKE — 食用贡献热力图</b>（点击展开）</summary>
<br/>
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Yht20927/Yht20927/output/snake-dark.svg"/>
    <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/output/snake.svg" alt="Contribution Snake"/>
  </picture>
</p>
</details>

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/divider.svg" width="100%" alt="—"/>
</p>

## 🗂 REPO MODULES · 仓库一览

### 🤖 Bridge Modules · 社媒自动化

| 项目 | 描述 | 核心能力 | ⭐ | 🍴 |
|---|---|---|:-:|:-:|
| [🎵 **douyin-cli**](https://github.com/Yht20927/douyin-cli) | 抖音全自动评论管理 | ReplyEngine · 图片评论 · 多账号 · SQLite schema v8 · 运营仪表盘 | `76` | `17` |
| [📕 **xiaohongshu-cli**](https://github.com/Yht20927/xiaohongshu-cli) | 小红书全自动管理 | 7 人格轮换 · 行为模拟 · 45-180s 随机 · 风控断路器 | `36` | `4` |
| [💼 **BossZhipin-cli**](https://github.com/Yht20927/BossZhipin-cli) | BOSS直聘命令行工具 | 17 条命令 · 匹配评分 · 批量打招呼 · `@ref` 缓存 · 48s 写节流 | `22` | `8` |
| [📈 **ths-cli**](https://github.com/Yht20927/ths-cli) | 同花顺行情 / 量化 CLI | 20+ 命令 · 14 项指标 · 6 策略回测 · 盘中 `watch` · 组合风控 | `13` | `1` |
| [🎬 **tiktok-cli**](https://github.com/Yht20927/tiktok-cli) | TikTok 全自动评论管理 | 读 / 写接口实测 · SecSDK 头 · 长串关联缓存 · v0.3 | `2` | — |

### 🎬 媒体与创作

| 项目 | 描述 | 核心能力 | ⭐ | 🍴 |
|---|---|---|:-:|:-:|
| [🎥 **douyin-living**](https://github.com/Yht20927/douyin-living) | 抖音直播录制 + 多模态 AI 切片 | 4K FLV 录制 · 弹幕 WebSocket · faster-whisper / WhisperX · 3 层 AI + 7 项数学融合 · ffmpeg 无损剪辑 | `49` | `6` |

### 🧠 AI Agent 基础设施

| 项目 | 描述 | 核心能力 | ⭐ | 🍴 |
|---|---|---|:-:|:-:|
| [🧠 **my-claude-memory**](https://github.com/Yht20927/my-claude-memory) | Agent 分层记忆管理 | 纯 Bash 4.0+ · 312/312 测试 · L1-L4 分层 · SHA-256 增量 · flock 并发 · 回收站 | `5` | `1` |

### 🔧 效率工具

| 项目 | 描述 | 核心能力 | ⭐ | 🍴 |
|---|---|---|:-:|:-:|
| [📝 **markdown-to**](https://github.com/Yht20927/markdown-to) | md-to.com 的本地 CLI 复刻 | 16 个工具 · 29 个 PDF 主题 · 84 个回归测试 · 100% 本地运行 | `3` | — |

### 🔬 安全研究

| 项目 | 描述 | 核心能力 | ⭐ | 🍴 |
|---|---|---|:-:|:-:|
| [🛡 **finalGraduationProject**](https://github.com/Yht20927/finalGraduationProject) | 源码级恶意代码智能检测与定位 | UniXcoder 768d · Graph-RAG 跨文件上下文 · LoRA · 双通道门控融合 · 4 语言 | `1` | — |

> 除特别说明外，Bridge 系列均为 MIT License；所有工具仅用于**本人账号**的合规运营与学习研究。

## 🔭 NOW · 正在做

- 📈 **ths-cli 持续迭代** — 科创板指数、资金流排行、盘中 `watch` 边沿告警，把「破止损必走」提前到破位瞬间
- 🎵 **douyin-cli 多账号** — `accounts` / `--account` / `videos` 收尾，多号并行驱动与独立记忆
- 🎬 **AI 视频管线** — 一句话想法 → 口播稿 → 整篇 TTS 配音 → whisper 对齐 → 富视觉渲染，产出「非网页风」成片
- 🛡 **源码安全研究** — 从「结果导向」转向「过程导向」的恶意代码检测范式

## 📫 CONTACT

- GitHub: [@Yht20927](https://github.com/Yht20927) — 欢迎 star、issue 和 PR，一起让浏览器自动化更可靠 🌱

<p align="center">
  <img src="https://raw.githubusercontent.com/Yht20927/Yht20927/main/assets/footer.svg" width="100%" alt="footer — real browsers, not simulation"/>
</p>
