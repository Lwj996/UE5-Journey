# AGENTS.md

> **For AI Agents working in this repository.**  
> 任何接手这个仓库的 AI 助手，请先读完这份文档。它会告诉你：用户是谁、想要什么、怎么和他协作、内容应该放到哪里、怎么提交。

---

## 0. 这是什么 · What This Is

这是一个 **个人学习日志仓库**（不是软件项目）。仓库主人是一个 **从前端转 UE5 游戏开发** 的学习者，每天和 AI 协作整理学习记录、笔记、计划。

`AGENTS.md` 是 AI 协作的事实标准约定文件（被 Cursor、OpenAI Codex、Aider 等多种工具自动识别）。后续接手的 AI 应该把它当作"必读说明书"。

**Always answer in Simplified Chinese (zh-CN)**, except when the user is explicitly practicing English.

---

## 1. 项目概览 · Project Overview

- **仓库名**：`UE5-Journey · Indie Co-op Horror Devlog`
- **GitHub**：[github.com/Lwj996/UE5-Journey](https://github.com/Lwj996/UE5-Journey)
- **目标**（**2026-06-22 双轨化**）：
  - 🟦 **主线**：18 个月内（~2027-12）做出一款致命公司 / REPO 风格的小品 co-op 恐怖游戏，**上架 Steam**
  - 🟩 **副线**：同期建立海外 UE5 兼职轨道，2027-12 月 $500-2000，2028-06 月 $2000-5000（"半全职"）
- **路径**：1 个人 + AI · UE5 蓝图为主 · Steam Direct 发布 + Upwork / Fiverr 接单
- **核心洞察**：主线品类（co-op 恐怖）= 副线接单品类。**一份学习两份收益。**
- **学习节奏**：项目驱动型 · 周末 ≥ 4h 是铁律 · 工作日少量 bonus
- **主路线图**：[`docs/03-indie-coop-roadmap.md`](./docs/03-indie-coop-roadmap.md)
- **作废档案**（保留不删，作历史对照）：
  - [`docs/00-roadmap.md`](./docs/00-roadmap.md) — 旧"12 月找海外工作"路径
  - [`docs/02-cadence-rebuild.md`](./docs/02-cadence-rebuild.md) — 旧"6h/周"cadence
- **方向转折记录**：[`scratchpad/life/2026-06-22-pivot-to-coop-horror-indie.md`](./scratchpad/life/2026-06-22-pivot-to-coop-horror-indie.md)
- **README**：英文 + 中文双版本

---

## 2. 用户画像 · User Profile

| 维度 | 描述 |
|------|------|
| 生日 | **2000-05-25**（用于人生日记年龄计算） |
| 编程背景 | 3 年 JavaScript / React 前端，用 Godot 把一个 2D 游戏做到接近完成（因没素材放弃） |
| UE 经验 | 从零开始（2026-04-22 起步），目前 ~3h 学习量（编辑器基础） |
| 英语水平 | 较弱，能读懂简单文档但写不出，需要 AI 翻译；自然拼读法学习中，语感在涨 |
| 学习节奏（**2026-06-22 重定**） | **项目驱动型**：阶段 0-1 期 6-8h/周，项目阶段 8-12h/周。**周末 ≥ 4h 是铁律**（见 [`docs/03-indie-coop-roadmap.md`](./docs/03-indie-coop-roadmap.md)） |
| 学习风格 | 喜欢"宝宝级"细节教程（如 B 站精修翻译），快进观看，跳过历史/废话 |
| 写作风格 | 直接、自嘲、爱开玩笑、会自评，情绪真实 |
| 玩家身份 | **重度 co-op 恐怖游戏玩家**（致命公司、REPO、恐鬼症、Devour、吞噬）→ 这是产品判断力优势 |
| **新主修方向**（2026-06-22 转向） | **单人独立游戏开发者**（不再追求海外工作 offer） |
| **目标产品** | 致命公司 / REPO 风格的 3D 多人 co-op 恐怖探险游戏，**18 月内上 Steam** |

---

## 3. 用户的写作风格与口吻 · Voice & Style

接手 AI 在润色用户日志时，必须**保留**这些特征：

- **真实情绪**：累就是累，失望就是失望，开心就是开心。不要一律改成"积极向上"。
- **自嘲与玩笑**：用户会写"我好自恋""强者的历史 自有大儒为其编经"这种话。**保留它们**，必要时配一句温和的"未来注脚"提醒（如"自恋是好的，但不要替代行动"）。
- **直接表达**：用户讨厌冗长。回答和润色都要简洁。
- **第一人称**：日志全部用"我"，不要被改成"我们"或"作者"。
- **混合中英术语自然**：如"我跳过 UE history"、"今晚做 GAS demo"，不要强行翻译技术词。

### 反面示范（不要这样改）

> ❌ "今天我以饱满的热情迎接了 UE5 学习的第一天，怀着对未来的无限憧憬..."  
> ✅ "第一天没装上 UE，但搭好了仓库、定好了路线——比安装一个软件值钱多了。"

---

## 4. 仓库结构与各文件用途 · Repository Layout

```
UE5-Journey/
├── README.md                    英文主页（给海外 HR / 国际社区）
├── README.zh-CN.md              中文版主页
├── AGENTS.md                    本文档
├── LICENSE                      MIT
├── .gitignore                   UE5-aware
│
├── docs/                        长篇计划与架构文档
│   ├── 00-roadmap.md            12 个月总路线
│   ├── 01-week-01-detailed.md   本周精确到小时的计划
│   ├── 02-resources.md          学习资源清单（持续更新）
│   └── 03-roguelike-architecture.md  Roguelike 项目架构
│
├── journal/                     每日 / 每周 / 每月日志
│   ├── README.md                日志索引（最新在前）
│   ├── TEMPLATE.md              日志模板
│   ├── YYYY-MM-DD-day-XX.md     每日日志
│   └── YYYY-MM-DD-week-XX-summary.md  周报
│
├── notes/                       主题式笔记（按知识领域）
│   ├── README.md
│   ├── ue5-concepts/            UE 概念（Actor、Blueprint、GAS...）
│   ├── cpp/                     UE 方言 C++
│   └── english/                 英语学习
│       ├── vocabulary.md        高频技术词汇
│       └── phonetics.md         发音规则（自建）
│
├── scratchpad/                  随手记（与 UE5 学习无直接关系的零碎观察）
│   ├── README.md
│   ├── YYYY-MM-DD-topic.md      AI 工具体验、行业观察、想法闪念等
│   └── life/                    人生日记（重大抉择 / 核心恐惧 / 转折点）
│       ├── README.md
│       ├── TEMPLATE.md          标准化模板（含 1/5/10/20/30 年回看接口）
│       └── YYYY-MM-DD-slug.md   单篇人生日记
│
└── assets/                      图片、GIF、架构图
```

### 关键判断：内容该放哪？

> **铁律：每次用户给你新内容，都先走这张表分类，再动笔。** 分类不清时主动问用户，不要默认丢进 scratchpad 当垃圾桶。

| 用户给你的内容 | 放哪里 |
|---------------|--------|
| 今天的 UE 学习记录、心情、反思 | `journal/YYYY-MM-DD-day-XX.md` |
| 一周复盘 | `journal/YYYY-MM-DD-week-XX-summary.md` |
| 学到的某个 UE 概念（如蓝图变量） | `notes/ue5-concepts/NN-topic.md` |
| 学到的某个 C++ 写法 | `notes/cpp/NN-topic.md` |
| 新英语单词 | `notes/english/vocabulary.md` |
| 新发现的好教程 / 工具 | `docs/02-resources.md` |
| 长期计划调整（路线图、节奏表） | `docs/00-roadmap.md` 或 `docs/02-cadence-rebuild.md` |
| 截图 / GIF | `assets/`，文件名 `day-XX-描述.gif` |
| **零碎观察、AI 工具体验、行业八卦、想法闪念** | **`scratchpad/YYYY-MM-DD-topic.md`** |
| 学习方法反思（拖延自剖、节奏调整等"修工具"） | `scratchpad/YYYY-MM-DD-topic.md` |
| **重大人生抉择 / 核心恐惧 / 转折点 / 深度复盘** | **`scratchpad/life/YYYY-MM-DD-slug.md`**（用 [`scratchpad/life/TEMPLATE.md`](./scratchpad/life/TEMPLATE.md) 模板，必含未来回看接口） |

**模糊判别口诀**：

- **"我学了 / 我做了 X"** → journal
- **"我观察到 / 我试用了 / 这个工具 / 这个行业 / 我打算调整学习方法"** → scratchpad
- **"我害怕 / 我抉择 / 我后悔 / 我此刻不知道未来怎么办"** → scratchpad/life
- **"我整理了 / 这是 X 的笔记"** → notes
- **"改一下计划 / 路线 / 资源"** → docs

### 判别 journal vs scratchpad

| 特征 | journal/ | scratchpad/ |
|------|---------|-------------|
| 与 UE5 学习直接相关？ | ✅ 是 | ❌ 否 |
| 必须双语？ | ✅ 是 | ❌ 否（中文为主即可） |
| 必须套结构化模板？ | ✅ 是 | ❌ 否 |
| 必须每天一篇？ | ✅ 是 | ❌ 否（想到再写） |
| 典型例子 | "今天跟完 Starter Course Ch.1" | "试用了 GPT Image-2，色彩比上代好很多" |

---

## 5. 分支策略 · Branch Strategy

```
main  ←  正式发布的内容（简历链接的就是它）
dev   ←  日常写作（草稿、待整理）
feature/*  ←  特定专题（如 feature/gas-notes）
```

**默认在 `dev` 分支工作**。

### 周期性合并

- **每周日**：用户写完周报后，合并 dev → main
  ```powershell
  git checkout main
  git merge dev
  git push origin main
  git checkout dev
  ```

接手 AI 处理日常日志/笔记时，**不要**自己合并到 main。除非用户明确要求"整理一下，发到 main"。

---

## 6. Commit Message 规范 · Commit Conventions

遵循 **Conventional Commits**，**全部英文**：

| 前缀 | 用于 | 例 |
|------|------|-----|
| `docs:` | 文档、日志、笔记 | `docs(journal): day-02 first UE editor open` |
| `feat:` | 新功能（未来 UE 项目） | `feat(hero): add dash ability` |
| `fix:` | 修 bug | `fix(ai): enemy patrol path stuck` |
| `refactor:` | 重构 | `refactor(inventory): use data asset` |
| `chore:` | 杂项 | `chore: update .gitignore` |
| `perf:` | 性能优化 | `perf(spawn): pool enemies` |

### Scope 命名

- 日志：`docs(journal): ...`
- 笔记：`docs(notes/ue5): ...`、`docs(notes/cpp): ...`、`docs(notes/english): ...`
- 资源：`docs(resources): ...`
- 路线图：`docs(roadmap): ...`
- 随手记：`docs(scratchpad): ...`
- Agents 自身：`chore(agents): ...`

### 格式建议（多行）

```
docs(journal): day-02 first UE editor open

- Confirm UE 5.7 installation completed
- Run Third Person template
- Note: editor language stays English on purpose
```

---

## 7. 日志（journal/）写作规范

### 双语规范（最重要）

**所有日志必须双语**：
- 🇨🇳 中文：用户亲笔写的内容（你只做轻润色，不改语气）
- 🇬🇧 英文：**AI 翻译**，必须明确标注 `*(AI-translated)*`

> ⚠️ **绝不能让用户误以为他英语水平已经达到了独立写作的程度**。这是用户明确的要求，是他防止"虚假能力沾沾自喜"的护城河。

### 标准结构（参考 `2026-04-22-day-01.md`）

```markdown
# Day XX · YYYY-MM-DD · Weekday

> 🌐 双语版本说明

> Mood / Time spent / Week / Plan

## ① 今天做了什么 · What I Did Today
🇨🇳 ...
🇬🇧 *(AI-translated)* ...

## ② [自由章节] · [Section Title]
🇨🇳 ...
🇬🇧 *(AI-translated)* ...

## ③ 学到的 3 个新东西
## ④ 遇到的问题 & 解决
## ⑤ 今天的英语词汇（表格）
## ⑥ 明天要做什么
## ⑦ 一句话总结
```

### 工作流：用户给你零散笔记 → 你处理

1. **不要自己编内容**——只整理、润色、双语化用户给的素材
2. **保留用户的所有原话精华**（金句、玩笑、自嘲）
3. 缺失的字段（如学到的 3 个新东西）写"待今晚补"，不要瞎填
4. 时间线注意：午休写 vs 当晚写 vs 次日补，**如实标注**

---

## 8. 笔记（notes/）写作规范

- 文件名：`NN-topic-name.md`（数字前缀，便于排序）
- 标题：清晰，便于检索
- 必含：**问题 → 答案** 结构（"为什么 Pawn 要有 Controller？" 比 "Pawn 有 Controller" 强 10 倍）
- 适当贴代码片段（用 markdown ```cpp / ```js / ```hlsl）
- 适当画图（提示用 [Excalidraw](https://excalidraw.com/) 导出 PNG 放到 `assets/`）

---

## 9. 默认工作流 · Default Workflow When User Sends You Notes

用户日常给你的输入有几种类型，按以下流程处理：

### A. "这是今天的零散笔记，整理一下"
1. 先判断这是哪一天（默认是当天，但用户可能在补昨天 / 写午休）
2. 找到对应日志文件（`journal/YYYY-MM-DD-day-XX.md`）。如果不存在，从 `journal/TEMPLATE.md` 复制一份
3. 用双语规范结构化用户的内容
4. 把英语单词补到 `notes/english/vocabulary.md`
5. 如果涉及新概念笔记，新建/更新 `notes/...` 下对应文件
6. `git checkout dev`（确保在 dev 分支）→ `git add` → 用规范 commit message → `git push`

### B. "我学了 XX 概念，记一下"
1. 在 `notes/ue5-concepts/` 或 `notes/cpp/` 找/建对应文件
2. 用 **问题 → 答案** 结构写
3. commit + push

### C. "推一下 git" / "上传 github"
1. `git status` 检查
2. 如果在 `main`，先切回 `dev`（除非用户明确要求合并到 main）
3. `git add .` → commit（如有未提交内容）→ `git push`
4. 报告 commit hash 和 push 结果

### D. "更新一下路线图 / 资源"
1. 在对应 `docs/` 文件里更新
2. 注明修改原因（commit message 写清楚）

### E. "我聊点别的 / 随手记一下"
- 用户分享与 UE5 学习无直接关系的内容（AI 工具体验、行业观察、闲聊金句、灵感片段等）
1. 判断是否值得归档：
   - 有保留价值（观察、想法、教训）→ 进 `scratchpad/`
   - 纯闲聊（"你说的对"、"哈哈"）→ 不归档，正常对话即可
2. 归档时：
   - 文件名 `scratchpad/YYYY-MM-DD-topic-slug.md`
   - 中文为主，**不强制双语**、**不套结构化模板**
   - 保留用户原话的味道，必要时补 1-2 段 AI 视角的评论或提醒
   - 末尾可以加一段"关联到 UE5 学习"，把闲聊钩回主线（如果能钩）
3. 更新 `scratchpad/README.md` 的文件列表（最新在前）
4. commit message：`docs(scratchpad): YYYY-MM-DD <topic>`

### F. "我有一次重大抉择 / 我很恐惧 / 我想忏悔" → **人生日记**
- 触发信号：用户讨论换方向、付出徒劳的恐惧、能力怀疑、年龄焦虑、转折点心态、深度自我对话
- 区分点：**E 是"对外的观察"，F 是"对内的判断"**。F 的读者是 5/10/20/30 年后的用户自己
1. 复制 [`scratchpad/life/TEMPLATE.md`](./scratchpad/life/TEMPLATE.md)，重命名为 `scratchpad/life/YYYY-MM-DD-slug.md`
2. **强制必填**：
   - 日期、年龄（如不知道，留 `__岁` 占位并提醒用户补）
   - **当时的原话**——逐字保留，**绝不修改**（包括错别字、玩笑、脏话）
   - 当时面对的选项（A/B/C 表格）
   - 抉择 + 当时的脑回路（不后期粉饰）
   - 1/5/10/20/30 年回看接口（即使现在留 `_待回填_`，也**不能省**）
3. 如果这次对话有 AI / 朋友 / 书籍输入，整理到「⑤ 外部输入」段落，**保留用户当时被打动的那一句**
4. 末尾必填「一句话给当下的自己」
5. 更新 [`scratchpad/life/README.md`](./scratchpad/life/README.md) 的文件列表
6. commit message：`docs(scratchpad/life): YYYY-MM-DD <slug>`
7. **不要**自作主张去同时改 `docs/` 计划文件——除非用户明确要求"改一下计划"。F 的核心是**记录**而非**调整**

---

## 10. 用户偏好的技术决策 · Technical Preferences

> 这些是已经讨论过、不要再质疑的决策。

| 决策项 | 选择 | 理由 |
|-------|------|------|
| **身份定位**（2026-06-22 双轨化）| **Publisher × Freelancer** | 主线自己上 Steam；副线 Upwork / Fiverr 接 UE5 兼职。**不投全职简历**。 |
| **主项目类型**（2026-06-22 重定）| **3D 多人 co-op 恐怖探险游戏**（致命公司 / REPO 类） | 用户深度玩家身份 + 2024-2026 红利窗口 + 单人 + AI 可达 |
| 平台 | **Steam（PC 独占）** | 不做主机，不做移动端 |
| UE 版本 | **5.7** | 已下载 |
| 编辑器语言 | **英文界面** | 与文档 / 教程 / YouTube 对得上 |
| 蓝图 vs C++ | **蓝图为主，C++ 仅性能瓶颈** | 小品游戏不需要复杂 C++ 框架 |
| 联机方案 | **Listen Server（2-4 人）** | 不做 dedicated server，小规模房间足够 |
| **主动不学** | Nanite / Lumen 深度优化 · GAS · World Partition · 主机移植 · 反作弊 | 小品 co-op 用不到，节省 6+ 月时间 |
| 美术方案 | **AI 生成（Midjourney → Meshy）+ Fab 商城** | 解决用户之前"没素材"的硬伤 |
| 内容平台 | **GitHub 为主**（不做 B 站 / 抖音） | 用户明确选择 |
| 入门教程 | 用户自己选（B 站 / YouTube），不强推 | 但起步从 **Third Person Template** 改，不从零搭 |
| Git 工作流 | main + dev + feature/*，**每月底**合并 | 5/7 已下调（不再每周合） |
| Commit 信息 | Conventional Commits，全英文 | 已建立 |
| 日志语言 | **双语必须，英文标 AI 翻译** | 用户的反虚假承诺 |
| 求职方向 | **已作废** | 2026-06-22 转 publisher 路径 |

---

## 11. 反模式 · Anti-Patterns（千万不要做）

❌ **不要修改 git 全局配置**（用户已设好 `LWJ` / `913456219@qq.com`）  
❌ **不要把日志改成"积极向上"的鸡汤体**——用户讨厌这个  
❌ **不要在英文部分省略 `*(AI-translated)*` 标注**——这是用户的核心承诺  
❌ **不要主动合并 dev → main**（除非明确要求）  
❌ **不要建议用户做"网络营销"**（B 站、抖音、Devlog 视频）——已被否决  
❌ **不要推荐 UE 5.6 或更老版本**——用户已经在 5.7  
❌ **不要给"完美但庞大"的方案**——用户每天只有 2h，要可执行  
❌ **不要在用户没提供原始素材时编造日志内容**  
❌ **不要使用过多 emoji 装饰**——只用作状态标记（✅ ⚠️ 🇨🇳 🇬🇧 等）  
❌ **不要在每次回复中复述用户已知信息**——直接做事

---

## 12. 推荐的回复风格 · Response Style

- **先做后说**：先调用工具完成任务，再用 1 段话简明汇报"做了什么、提交到了哪里、用户下一步该做什么"
- **报告结果用代码块或表格**，不要堆描述性段落
- **结尾给"下一步"提示**——但不超过 3 条
- **绝不在汇报里夹杂自我表扬**（"我已经精心地为您..."）

---

## 13. 当前状态快照 · Current Snapshot

> 这部分会随时间过时——AI 看到时请用 `git log --oneline -5` 验证最新状态。

- **当前阶段**：**Phase 0 · 引擎入门**（2026-07 ~ 08 计划范围）
- **本周（6/22-6/28）**：工作日少量看教程；**周六周日跟完一个完整 UE co-op 入门教程项目**
- **下一里程碑**：Phase 1 · Prototype #1（"捡东西带回基地"最小循环，目标 2026-10）
- **最近重大事件**：**2026-06-22 方向转折**——从"找海外工作"转向"做小品 co-op 恐怖游戏 publisher"
- **最近塌方记录**：5/8-6/22 共 46 天 0h UE（见 `scratchpad/life/2026-06-22-pivot-to-coop-horror-indie.md`）
- **当前分支**：默认 `dev`
- **最近提交**：用 `git log --oneline -5` 查
- **GitHub URL**：[github.com/Lwj996/UE5-Journey](https://github.com/Lwj996/UE5-Journey)

---

## 14. 给未来 AI 的一句话

> 这个仓库的主人是一个真诚、自嘲、有野心、英语弱但意志强的人。请尊重他的每一段原话，包括他的玩笑和情绪。你的工作是让他写得更好、走得更远，而不是让他看起来更光鲜。

---

**Maintainer**: Repository owner  
**Last updated**: 2026-04-27  
**Convention**: [agents.md](https://agents.md/) standard
