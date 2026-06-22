# UE5-Journey · 独立 Co-op 恐怖游戏开发日志

> **一个人 + AI 用 Unreal Engine 5 做小品级 co-op 恐怖游戏，目标 18 月内上 Steam。**
> 参照：致命公司 / REPO / Content Warning / 恐鬼症。

[English](./README.md) | 简体中文

---

## 关于

我是 **25 岁前端工程师**，3 年 React 经验，2026-06-22 正式转向**单人独立游戏开发**。
之前两次走偏（最初目标是海外 gameplay 程序员岗），6/22 那天看清了：

> **我不是在找一份工作 offer，我是在做一款我自己想上 Steam 的游戏。**

这个仓库是我的公开 devlog：代码、笔记、人生日记全在一起——给 5/10/30 年后的我看。

**背景**
- 3 年前端（JavaScript / React）
- 用 Godot 把一个 2D 游戏做到接近完成（因为没素材放弃——现在 AI 解决了）
- 重度 co-op 恐怖游戏玩家（致命公司、REPO、恐鬼症、Devour）
- 2026-04 从零起步学 UE5

---

## 真正的目标

**18 个月内，把一款小品级 3D co-op 恐怖游戏发到 Steam**（目标日：2027-12）。

参照作品：

| 游戏 | 团队 | 开发时间 | 战绩 |
|---|---|---|---|
| Lethal Company | **1 人** | ~2 年业余 | 发布 4 月 ≈ 4000 万美金 |
| Content Warning（链在一起） | 9 人 | ~1 年 | 免费送 24h → 600 万下载 |
| REPO | 小工作室 | ~1.5 年 | 2025 Q1 爆款 |

共同特征：**4-8 人 co-op · 物理互动 · 恐怖 + 搞笑 · 低多边形美术 · 单人开发者可达**。

完整路线：[`docs/03-indie-coop-roadmap.md`](./docs/03-indie-coop-roadmap.md)

---

## 18 月路线（高层）

| 阶段 | 月份 | 产出 |
|---|---|---|
| 0 · 引擎入门 | 2026-07 ~ 08 | 3 人能联机走来走去 |
| 1 · 原型 #1 | 2026-09 ~ 10 | "捡东西带回基地"最小核心循环上 itch.io |
| 2 · 原型 #2 | 2026-11 ~ 2027-01 | 加恐怖层（黑暗 / 音效 / 1 个怪物） |
| 3 · Demo v0 | 2027-02 ~ 06 | **上 Steam Next Fest** |
| 4 · 完整版 | 2027-07 ~ 12 | **上架 Steam，$5-10** |

---

## "一个人 + AI" 在 2026 是可行的

| 任务 | AI 工具 |
|---|---|
| 代码（蓝图 / C++ 调试） | Cursor + Claude |
| 美术（概念 → 3D 模型） | Midjourney → Meshy |
| 音效 | ElevenLabs |
| 音乐 | Suno / Udio |
| 宣传片 / 商店页 | Runway / Veo + Claude |
| 本地化 | Claude |

18 月工具预算：**约 $1200 (8500 RMB)**。Steam 卖 200 份 $5 即回本。

---

## 周节奏（项目驱动）

```
工作日   1-2 晚 × 30-60min   （可选，bonus）
周六     ≥ 4h               （铁律）
周日     3-5h
─────────────────────────────────
总计     8-12h / 周（项目阶段会自然涨）
```

**铁律**：周六 ≥ 4h。没有这个，18 月计划不成立。

---

## 路线图

| 阶段 | 月份 | 重点 |
|------|------|------|
| 1. 基础 | 1 - 2 | 编辑器、蓝图、Actor 框架 |
| 2. C++ 入门 | 3 | UE 方言 C++（UCLASS、UPROPERTY、UFUNCTION） |
| 3. 第一个真项目 | 4 - 6 | 俯视角 Roguelike（可玩 + 发布） |
| 4. 工业化技能 | 7 - 9 | GAS、Replication、Unreal Insights |
| 5. 求职期 | 10 - 12 | 作品集精修、投简历、面试 |

完整计划：[`docs/00-roadmap.md`](./docs/00-roadmap.md)

---

## 当前进度

- [x] 环境搭建（UE 5.7 + Visual Studio 2022）
- [x] Epic 账号绑定 GitHub
- [x] 编辑器基础（界面 / view mode / snap / duplicate）
- [x] **方向确认（2026-06-22）**：单人 co-op 恐怖独立游戏，不是找工作
- [ ] 阶段 0 · 跟完第一个完整教程项目（目标：6/27-6/28 周末）
- [ ] 阶段 0 · 3 人联机 "走来走去" demo
- [ ] 阶段 1 · 第一个可玩原型上 itch.io
- [ ] 阶段 3 · 上 Steam Next Fest
- [ ] **阶段 4 · 上架 Steam**

---

## 仓库导航 · Repo Map

| 我想找... | 去哪里 |
|---|---|
| 今天 / 某天的 UE 学习记录 | [`journal/`](./journal/) |
| 长期计划、路线图、本周表 | [`docs/`](./docs/) |
| 整理好的知识笔记（UE / C++ / 英语） | [`notes/`](./notes/) |
| AI 工具体验 · 行业观察 · 学习方法反思 | [`scratchpad/`](./scratchpad/) |
| **人生抉择 · 核心恐惧 · 转折点**（5-30 年后回看） | [`scratchpad/life/`](./scratchpad/life/) |
| 截图 / GIF / 架构图 | [`assets/`](./assets/) |

详细路由规则与写作规范：见 [`AGENTS.md`](./AGENTS.md)。

## 仓库结构

```
UE5-Journey/
├── docs/                 长篇计划（路线图、节奏表、项目架构）
├── journal/              每日 / 每周学习日志（双语）
├── notes/                主题笔记（UE 概念、C++、英语词汇）
├── scratchpad/           随手记（与 UE5 学习无直接关系的零碎观察）
│   └── life/             人生日记（重大抉择 / 核心恐惧 / 转折点）
└── assets/               图片、GIF、示意图
```

---

## 技术栈（为单人 co-op 恐怖游戏聚焦）

**引擎**：Unreal Engine 5.7 · 蓝图优先 · C++ 仅性能瓶颈
**联机**：Listen Server（2-4 人）· Online Subsystem Steam
**AI 工作流**：Cursor · Claude · Midjourney · Meshy · ElevenLabs · Suno
**工具**：Visual Studio 2022 · Git · Steam Direct

**主动不学**（小品 co-op 用不到）：Nanite/Lumen 深度优化 · GAS · World Partition · 主机平台移植 · 反作弊系统。

---

## 联系方式

- GitHub：当前页面
- Email：_待填_
- LinkedIn：_待建_

---

## 许可证

代码片段：[MIT License](./LICENSE)  
文字笔记：[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
