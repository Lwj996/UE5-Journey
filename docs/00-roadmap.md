# 12 个月路线图

> 从零到能投海外初级 Gameplay Programmer 岗位。每周 22 小时。

## 总览表

| 月 | 主题 | 关键产出 | 时间投入 |
|----|------|---------|---------|
| 1 | 编辑器 + 蓝图基础 | 第三人称小场景 | 88h |
| 2 | 动画 + AI + UI | 5 分钟可玩 Demo | 88h |
| 3 | UE C++ 入门 | 蓝图 Demo 的一半改 C++ | 88h |
| 4 | Roguelike - 架构 | 核心系统设计 + 角色控制 | 88h |
| 5 | Roguelike - 战斗 | GAS 集成 + 技能/Buff | 88h |
| 6 | Roguelike - 生成与发布 | 过程生成 + itch.io 发布 | 88h |
| 7 | 联机复制 | 双人合作模式 | 88h |
| 8 | 性能优化 | Unreal Insights 优化日志 | 88h |
| 9 | 工具链 + Python | 编辑器脚本、自动化工具 | 88h |
| 10 | 作品集精修 | 全项目重构、视频录制 | 88h |
| 11 | 求职材料 | 英文简历、LinkedIn、外包试水 | 88h |
| 12 | 投递与面试 | 海外岗位 + 外包 | 88h |

---

## 第 1 个月：编辑器 + 蓝图基础

**目标**：会用 UE 编辑器，能用纯蓝图做一个第三人称可交互小场景。

### 必学知识点
- [ ] 编辑器四大面板：Viewport、Outliner、Details、Content Browser
- [ ] 核心类体系：`Actor` / `Pawn` / `Character` / `Controller` / `GameMode` / `PlayerState`
- [ ] 蓝图：变量、函数、事件、接口（BPI）、事件分发器（Event Dispatcher）
- [ ] Cast 与继承
- [ ] Trace（LineTrace、SphereTrace）
- [ ] Collision 通道与响应
- [ ] UMG 基础（血条、简单菜单）

### 月末里程碑
做一个小场景：
- 一个可走可跳的角色
- 5 种可交互物体（门、开关、拾取物、陷阱、NPC）
- 一个简单 HUD
- 能打包成 .exe 跑起来

### 推荐资源
- Epic 官方 [UE 5.7 Starter Course](https://dev.epicgames.com/community/learning/tutorials/bE7Z/unreal-engine-5-7-starter-course)
- YouTube: Gorka Games、Matt Aspland（俯视角 Roguelike 教程多）

---

## 第 2 个月：动画 + AI + 打包

### 必学
- [ ] 动画蓝图、状态机、Blend Space
- [ ] IK Retargeter（把 Mixamo 动画迁移到 UE 角色）
- [ ] Behavior Tree、Blackboard、EQS（AI 三件套）
- [ ] Niagara 基础（一个爆炸特效就够）
- [ ] UMG 完整流程（主菜单、暂停菜单、死亡界面）
- [ ] 关卡流送 / World Partition 基础

### 里程碑
5 分钟可玩的"小怪追我我打小怪"Demo，打包成 .exe 发给朋友玩。

---

## 第 3 个月：C++ 入门

**只学 UE 方言的 C++，不学标准 C++**，能省一半时间。

### 必学
- [ ] `UCLASS` / `UPROPERTY` / `UFUNCTION` 三大宏
- [ ] UE 容器：`TArray` / `TMap` / `TSet` / `FString`（**不要用 `std::vector`**）
- [ ] `UObject` 与垃圾回收
- [ ] `USTRUCT` 结构体
- [ ] 指针类型区分：
  - 原始指针 `T*`（配合 `UPROPERTY()` 防止被 GC）
  - `TWeakObjectPtr<T>`
  - `TSharedPtr<T>` / `TSharedRef<T>`
- [ ] 蓝图与 C++ 交互：C++ 暴露函数给蓝图、蓝图继承 C++ 类
- [ ] Delegate（单播、多播、动态）

### 里程碑
把第 2 个月的蓝图 Demo 的核心系统改成 C++（至少角色基类、物品系统、伤害逻辑三样）。

### 推荐资源
- **Stephen Ulibarri《Unreal Engine 5 C++ Developer》**（Udemy，40h，英文，国际公认最好入门课）
- 官方文档：[Unreal Engine C++ Programming Tutorials](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-c-plus-plus-programming-tutorials)

---

## 第 4 - 6 个月：俯视角 Roguelike 主项目

**这是你作品集的核心**。详细架构见 [`03-roguelike-architecture.md`](./03-roguelike-architecture.md)。

### 阶段里程碑
- 第 4 月末：角色能移动 + 攻击 + 检地敌人，数据驱动武器系统
- 第 5 月末：GAS 集成完成，5 个主动技能 + 10 个 Buff/Debuff
- 第 6 月末：过程生成房间 + 完整 UI + 存档 + itch.io 发布

---

## 第 7 个月：多人联机

海外招聘最稀缺的技能。

### 必学
- [ ] Replication 基础（`Replicated`、`RepNotify`）
- [ ] RPC：Server/Client/Multicast
- [ ] Authority / Autonomous / Simulated 权限模型
- [ ] Listen Server vs Dedicated Server
- [ ] Lag Compensation 基础认知

### 里程碑
把 Roguelike 加一个 2 人合作模式，局域网能打。

---

## 第 8 个月：性能优化

### 必学
- [ ] Unreal Insights 工作流
- [ ] `stat unit` / `stat gpu` / `stat game` 命令
- [ ] RenderDoc 抓帧分析
- [ ] Draw Call 优化（Instancing、HLOD）
- [ ] 内存分析（`Memreport`）
- [ ] LOD 与 Nanite 权衡

### 里程碑
写一篇英文 **Optimization Case Study**（优化案例分析），贴在 GitHub README。

---

## 第 9 个月：工具链与 Python

### 必学
- [ ] UE Python API 基础
- [ ] 写一个批量资产处理工具
- [ ] Editor Utility Widget（编辑器内的自定义面板）
- [ ] 简单的 C++ Editor 模块

### 里程碑
一个公开的小工具/小插件（开源到 GitHub）。

---

## 第 10 个月：作品集精修

- 把 Roguelike 代码**全面重构**到"业界水准"（现在再看第 4 月的代码，你会想吐）
- 录制 3 分钟 YouTube Demo 视频（英文配音/字幕）
- 每个仓库的 README 加 Gameplay GIF 和架构图

---

## 第 11 - 12 个月：求职

### 11 月：准备
- [ ] 英文简历（Overleaf Modern CV 模板）
- [ ] LinkedIn 英文档案完善
- [ ] ArtStation 页面
- [ ] Upwork 开始接小外包（积累 rating）

### 12 月：投递
- [ ] Hitmarker.net（游戏专）
- [ ] Work With Indies
- [ ] LinkedIn / Indeed / Glassdoor
- [ ] Remote Game Jobs
- [ ] 目标：每周投 10 家，月末至少 1 轮面试

---

## 铁律

1. **每周至少 8 小时做自己的项目**，不是单纯跟教程
2. **每天 1 次 commit**，哪怕只改一行字
3. **遇到问题先英文搜索**（`site:forums.unrealengine.com` 或 `site:dev.epicgames.com`）
4. **所有技术笔记记在 `notes/` 里**，未来翻倍受益
5. **不要追求完美的代码**，第一版跑起来比什么都重要
