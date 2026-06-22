# 学习资源清单

> 分级整理，⭐ = 必看 · 🟦 = 主线（独立游戏）· 🟩 = 副线（接单）。
> **2026-06-22 重新整理**：适配新方向 "1 个人 + AI 做 co-op 恐怖游戏 + 海外 UE5 兼职" 双轨。详见 [`03-indie-coop-roadmap.md`](./03-indie-coop-roadmap.md)。
>
> **优先级变化（旧 → 新）**：
> - 多人联机：第 7 月起 → **第 1-2 月即上**（主线核心技能）
> - C++ / GAS：必学 → **降级**（GAS 已废，C++ 仅性能瓶颈）
> - 求职平台：核心 → **降级**（不投全职简历）
> - 接单平台：**新升一级**（副线主战场）
> - **co-op 恐怖游戏专项**：**新增**（主线品类）

---

## 🟦 主线 · 引擎核心资源

### 官方（最权威）

- ⭐ [Epic Developer Community](https://dev.epicgames.com/community/) — 官方学习平台
- ⭐ [UE 5.7 Starter Course](https://dev.epicgames.com/community/learning/tutorials/bE7Z/unreal-engine-5-7-starter-course) — 零基础入门课（英文）
- [Official Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/) — 文档（英文）
- [Unreal Engine Learning Hub](https://www.unrealengine.com/en-US/onlinelearning-courses) — 免费官方课
- [Inside Unreal (YouTube)](https://www.youtube.com/@UnrealEngine/playlists) — Epic 工程师直播

### 🟦 多人联机（主线核心 · 阶段 0-1 即上）

> **本项目核心技能** —— co-op 游戏 = 联机 = 必学。

- ⭐ Stephen Ulibarri《Multiplayer Steam Subsystem》— Udemy
- ⭐ [Cobra Code (YouTube)](https://www.youtube.com/@CobraCode) — UE5 联机专精
- [UE Networking Docs](https://dev.epicgames.com/documentation/en-us/unreal-engine/networking-and-multiplayer-in-unreal-engine)
- [Advanced Steam Sessions Plugin](https://www.fab.com/listings/0c47e02e-5b1c-4cd9-a0c5-7c2c2c2c2c2c) — Fab 商城（占位链接，到时实搜）

### 蓝图教程（主战场，90% 时间）

- ⭐ [Matt Aspland (YouTube)](https://www.youtube.com/@MattAspland) — 蓝图 101 最全
- ⭐ [Ryan Laley](https://www.youtube.com/@RyanLaley) — 系统性教程
- [Gorka Games](https://www.youtube.com/@GorkaGames) — 新手友好
- [Reids Channel](https://www.youtube.com/@ReidsChannel) — 进阶技巧

### C++ 专项（降级 · 仅性能瓶颈时上）

- Stephen Ulibarri《Unreal Engine 5 C++ Developer》— Udemy（**不再必读**，备用）
- [UE C++ Programming Tutorials](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-c-plus-plus-programming-tutorials)
- Tom Looman 的博客：[tomlooman.com](https://www.tomlooman.com/) — 前 Epic 工程师，最好的 UE C++ 博客

### ❌ 已废 · 不再学的清单

> 这些是旧"找海外 gameplay 工作"路径下的必学项；新路径不需要。

- **GAS（Gameplay Ability System）** — 小品 co-op 用不到 → 旧资源（Tranek GAS Doc / Stephen GAS RPG 课）**不再列必看**
- 性能优化深度（Insights / RenderDoc 帧分析） — 小品 low-poly 不需要
- 大世界 World Partition / Nanite / Lumen 深度优化

---

## 🟦 主线 · co-op 多人合作恐怖游戏 · 专项资源（2026-06-22 新增）

> 这是本项目品类的针对性资源。**主线进入阶段 0 后优先看**。

### 品类参照游戏

| 游戏 | 价值 | 玩法核心 |
|---|---|---|
| **Lethal Company** | 1 人开发标杆 | 4 人 co-op、捡物品、计数返回、恐怖循环 |
| **REPO** | 物理互动 + 搞笑传播 | 物理拖动、嘴炮通信、阴间幽默 |
| **Content Warning（链在一起）** | 摄像 + 任务 + 病毒传播 | 拍恐怖视频、上传得分、关注度系统 |
| **Phasmophobia** | 道具驱动恐怖标杆 | 鬼物识别、调查证据、近距离通信 |
| **Devour** | 节奏型恐怖 | 逃跑 + 收集 + 仪式 |
| **吞噬（中文恐怖）** | 国产参照、本地化 | 文化梗、剧情线索、psychological |

### 教程资源（搜索关键词）

- YouTube：`UE5 horror game tutorial`、`UE5 co-op multiplayer tutorial`、`UE5 Lethal Company clone`
- B 站：`UE5 恐怖游戏教程`、`UE5 多人联机`
- ⭐ [Smart Poly (YouTube)](https://www.youtube.com/@SmartPoly) — UE 5 多人游戏系列
- [Coqui Games](https://www.youtube.com/@coquigames) — UE 5 horror 教程（占位，到时实搜）

### 第一个原型推荐功能（阶段 1，2026-09-10）

- First-Person Character Controller（Third Person Template 改）
- Flashlight + Battery system（手电筒电池）
- Pickup / Inventory System（捡物品、放进背包）
- Drop-off Zone（回收点 = 得分）
- Simple Enemy AI（听觉感知 / 简单追击）
- Voice Chat / Proximity Audio（近距离语音 = REPO 核心）

### 关键 Fab / 插件（阶段 1-2 用）

- [Fab](https://www.fab.com/) — 官方资产库（原 Quixel/Marketplace 合并）
- **Advanced Locomotion System** 或 **GASP**（Game Animation Sample Project）— 角色基础
- **Voice Chat（Online Subsystem）** — 玩家语音
- **Advanced Sessions Plugin** — Steam 联机房间

---

## 🟩 副线 · 接单平台与资源（2026-06-22 新增）

> 详细分析见 [`03-indie-coop-roadmap.md`](./03-indie-coop-roadmap.md) 「副线 · 海外 UE5 兼职轨道」段。

### 接单平台

- ⭐ [Upwork](https://www.upwork.com/) — 起步主战场，**阶段 0 即可注册（审号 1-2 周）**
- ⭐ [Fiverr](https://www.fiverr.com/) — 第一单破零最快，标准化 Gig
- [Toptal](https://www.toptal.com/) — 5 天 vetting，阶段 5+ 投
- [Lemon.io](https://lemon.io/) — 5 天 vetting，长期合同 9+ 月，阶段 5+ 投
- [Freelancer.com](https://www.freelancer.com/) — 价格战激烈，备用

### 独立游戏工作室招聘

- ⭐ [Work With Indies](https://workwithindies.com/) — 独立工作室 part-time / contract
- ⭐ [Epic UE Forums · Job Offerings](https://forums.unrealengine.com/c/community/job-offerings/) — 独立项目直接发帖
- [Remote Game Jobs](https://remotegamejobs.com/)
- [ArtStation Jobs](https://www.artstation.com/jobs)

### 国际收款工具（接单前必备）

- ⭐ [Wise (TransferWise)](https://wise.com/) — 多币种账户，费率最低
- [Payoneer](https://www.payoneer.com/) — Upwork / Fiverr 主流出金
- [PayPal](https://www.paypal.com/) — Fiverr 备用

### 个人作品集站

- [GitHub](https://github.com/) — 主站（仓库本身 = 主作品集）
- [itch.io](https://itch.io/) — 发布免费 prototype（阶段 1-2 用）
- [ArtStation](https://www.artstation.com/) — 美术 + 综合
- [LinkedIn](https://www.linkedin.com/) — 英文档案（接单时客户会看）
- 自建静态站（Vercel / Netlify 免费）— 阶段 3+

---

## 🟦🟩 AI 工具栈（详细见主 roadmap）

> 完整列表见 [`03-indie-coop-roadmap.md`](./03-indie-coop-roadmap.md) 「AI 工具栈」段。

- **代码**：Cursor + Claude / GPT-5 / Gemini
- **概念美术**：Midjourney v7+ / Stable Diffusion XL
- **图 → 3D 模型**：Meshy / TripoSR
- **音效**：ElevenLabs Sound
- **音乐**：Suno / Udio
- **配音**：ElevenLabs Voice
- **宣传片**：Runway / Veo
- **文案 / 翻译**：Claude

---

## 资产 / 素材

- ⭐ [Fab](https://www.fab.com/) — 官方资产库（**项目主用**）
- [Mixamo](https://www.mixamo.com/) — 免费动画库（Adobe 账号登录）
- [Sketchfab](https://sketchfab.com/) — 3D 模型库
- [Polyhaven](https://polyhaven.com/) — 免费 HDRI / 纹理 / 模型
- ⭐ **Meshy** + **Midjourney** — AI 生成（解决我之前"没素材"的硬伤）

---

## 英语学习工具（保留）

- ⭐ [Language Reactor](https://www.languagereactor.com/) — Chrome 插件，看 YouTube/Netflix 自动双语字幕
- [Anki](https://apps.ankiweb.net/) — 背单词，可自建 UE 词汇牌组
- [欧路词典](https://www.eudic.net/) — 划词翻译，PC 和手机同步
- ⭐ 自然拼读法（用户当前进度）— 见 [`notes/english/phonetics.md`](../notes/english/phonetics.md)

---

## 工具软件

### 必装

- **Visual Studio 2022 Community** — UE C++ 开发（即便 C++ 用得少，UE 默认要它）
- **Git + Git LFS** — 版本控制
- ⭐ **Cursor** — 主要 AI IDE（已订阅）

### 推荐

- **Rider for Unreal Engine**（付费）— 比 VS 好用的 IDE（可选）
- **ScreenToGif** — 录 GIF，做 portfolio / 商店页用
- **OBS Studio** — 录屏 / 直播（Devlog / 宣传片）
- **DaVinci Resolve** — 免费剪辑，Steam Trailer 用
- **Obsidian** — Markdown 笔记
- **Excalidraw**（网页版）— 画架构图
- **Blender** — 免费 3D 建模（备选；优先用 Meshy）

---

## ❌ 已降级 · 求职平台（全职岗，已不在主路径）

> **2026-06-22 起不再优先**。仅作为"5 年后路径转变"的备用清单留存。

- ~~[Hitmarker](https://hitmarker.net/) — 游戏行业专门求职~~
- ~~[LinkedIn Jobs](https://www.linkedin.com/jobs/) — 全职远程~~
- ~~[Indeed](https://www.indeed.com/) / [Glassdoor](https://www.glassdoor.com/)~~

---

**更新日志**：遇到新好资源随时添加，并 commit `docs(resources): ...`。
