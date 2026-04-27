# 第 1 周：精确到小时的计划（修订版）

> **原计划**：2026-04-22（Wed）~ 04-28（Tue）  
> **实际情况**：04-24（Fri）~ 04-26（Sun）未学习（玩游戏去了），原表从 Day 3 起未执行。  
> **修订后起止**：**2026-04-27（Mon）~ 2026-05-03（Sun）** —— 从今天起按本表执行，总投入仍为 **22h**。  
> **教程**：主跟 [B 站精修翻译 BV1qYSvBHELW](https://www.bilibili.com/video/BV1qYSvBHELW/)；需要对照英文界面时，可并行打开 [UE 5.7 Starter Course](https://dev.epicgames.com/community/learning/tutorials/bE7Z/unreal-engine-5-7-starter-course) 查章节名。

**已完成的进度（保留，不重做）**  
- Day 01 · 04-22：仓库、路线图、部分环境/下载  
- Day 02 · 04-23：教程选型、午休笔记（晚上若未补全，可在 Day 3 顺带补一句）

---

## 时间表总览（修订）

| 学习日 | 日期 | 星期 | 时长 | 主题（接续原 Day 3 起） |
|--------|------|------|------|-------------------------|
| Day 03 | **04-27** | Mon | 2h | 编辑器导航 + 快捷键 + `01-editor-basics.md` |
| Day 04 | **04-28** | Tue | 2h | Actor 放置 / 关卡里摆东西（Ch.3 类内容） |
| Day 05 | **04-29** | Wed | 2h | 继续 Ch.3 + 开做「小场景」 |
| Day 06 | **04-30** | Thu | 2h | 小场景收尾 + **录 GIF** |
| Day 07 | **05-01** | Fri | 2h | 蓝图入门：变量、BeginPlay、Tick、Print |
| Day 08 | **05-02** | Sat | 6h | 闪烁方块练习 + `02-actor-framework.md` 图 + 蓝图变量/函数 |
| Day 09 | **05-03** | Sun | 6h | Event / Dispatcher / BPI + **Week 1 周报** + `dev` → `main` |
| **合计** | | | **22h** | |

---

## Day 03 · 04-27 Mon · 2h · 编辑器导航

### 任务
- [ ] **0:00 - 0:05** 打开 `journal/2026-04-27-day-03.md`，写两句：空档三天、今天回到学习（不自我攻击，只记录事实）
- [ ] **0:05 - 1:35** B 站教程：**编辑器 / 视口 / 大纲 / 细节 / 内容浏览器** 相关章节（快进可以，**快捷键部分慢放**）
  - 练熟：`W/E/R`、`F`、`G`、`Alt + 鼠标`、Content Browser 搜索
- [ ] **1:35 - 1:50** 新建或更新 `notes/ue5-concepts/01-editor-basics.md`（至少 5 个面板英文名 + 1 句干啥用的）
- [ ] **1:50 - 2:00** 日志双语补全、`git commit` + `push`

---

## Day 04 · 04-28 Tue · 2h · Actor 与放置

### 任务
- [ ] **0:00 - 1:40** 跟教程：**往关卡里放 Actor、移动/旋转/缩放、简单打光**（对应 Starter Course Ch.3 一类内容）
- [ ] **1:40 - 1:50** 往 `01-editor-basics.md` 加 3 条「我今天点过的菜单英文名」
- [ ] **1:50 - 2:00** 日志 + commit + push

---

## Day 05 · 04-29 Wed · 2h · 小场景（上）

### 任务
- [ ] **0:00 - 1:45** 开做「小岛 / 小广场」任一场景：先堆 **10+** 个静态 Mesh（树、石、建筑均可）
- [ ] **1:45 - 2:00** 日志 + commit（可只提交文字；**大图/GIF 别强塞 Git**，放 `assets/` 即可）

---

## Day 06 · 04-30 Thu · 2h · 小场景（下）+ GIF

### 任务
- [ ] **0:00 - 0:30** 补光：Directional Light + Sky Atmosphere（按教程来）
- [ ] **0:30 - 0:40** 放 **Player Start**，Third Person 或当前模板能 **Play 跑一圈**
- [ ] **0:40 - 1:20** 继续加到 **20+** 个 Actor，整体能看
- [ ] **1:20 - 1:50** [ScreenToGif](https://www.screentogif.com/) 录 **~10s**，保存 `assets/week01-scene.gif`（或类似命名）
- [ ] **1:50 - 2:00** 日志里嵌入 GIF 路径 + commit + push

---

## Day 07 · 05-01 Fri · 2h · 蓝图入门（上）

### 任务
- [ ] **0:00 - 1:40** 跟教程：**第一张蓝图、变量、Print String、Event BeginPlay、Tick（概念摸到即可）**
- [ ] **1:40 - 1:50** 计划：周末两天要攻「闪烁方块 + 继承关系图」
- [ ] **1:50 - 2:00** 日志 + commit + push

---

## Day 08 · 05-02 Sat · 6h · 闪烁方块 + Actor 框架图 + 蓝图函数

### 任务
- [ ] **0:00 - 2:30** 练习：**Tick + Sine（或教程同款）驱动材质**，做「会闪/会呼吸颜色」的方块
- [ ] **2:30 - 3:00** 休息
- [ ] **3:00 - 4:30** `notes/ue5-concepts/02-actor-framework.md`：**Actor / Pawn / Character / Controller / GameMode** 继承关系（Excalidraw 导出 PNG → `assets/`）
- [ ] **4:30 - 5:30** 补充：蓝图 **变量类型**、**自定义函数**（可跟 Matt Aspland Blueprint Basics 任一集，**英文**当听力）
- [ ] **5:30 - 6:00** 日志 + commit + push

---

## Day 09 · 05-03 Sun · 6h · 事件/接口 + 周报 + 合并 main

### 任务
- [ ] **0:00 - 2:00** **Custom Event vs Function**、**Event Dispatcher**、**Blueprint Interface（BPI）**（概念 + 小例子）
- [ ] **2:00 - 2:30** 休息
- [ ] **2:30 - 4:00** 在 `03-blueprint-basics.md`（可新建）里做 **JS ↔ UE** 对照表（EventEmitter、interface…）
- [ ] **4:00 - 5:30** 写 **`journal/2026-05-03-week-01-summary.md`**
- [ ] **5:30 - 6:00** 合并发布：
  ```powershell
  git checkout main
  git merge dev
  git push origin main
  git checkout dev
  ```

---

## 每日结束检查表

```markdown
- [ ] 3 个关键词（中英）→ `notes/english/vocabulary.md`
- [ ] 新概念 → `notes/ue5-concepts/`
- [ ] 至少 1 次 commit
- [ ] 当天 `day-XX` 日志已更新
```

---

## 疑难

1. **UE 装路径**：全英文路径，无空格。  
2. **GitHub 慢**：代理或 Watt Toolkit。  
3. **蓝图中途崩**：`Ctrl+S` 狂魔养成习惯。

---

**下周（Week 2）**：动画蓝图、Mixamo、Behavior Tree —— 等本周周报写完后再写 `02-week-02-detailed.md`。
