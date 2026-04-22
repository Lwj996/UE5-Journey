# 第 1 周：精确到小时的计划

> 目标：搭好环境，跑通 Epic 官方 Starter Course 前 4 章，写 4 篇日志。

## 时间表总览

| 日期 | 时段 | 主题 | 时长 |
|------|------|------|------|
| Day 1（今天 Wed） | 晚间 | 环境搭建 + 仓库初始化 | 2h |
| Day 2（Thu） | 晚间 | Epic 账号绑定 + 官方课 Ch.1 | 2h |
| Day 3（Fri） | 晚间 | 官方课 Ch.2（UE 界面导航） | 2h |
| Day 4（Sat） | 全天 | 官方课 Ch.3 + 第一个小场景 | 6h |
| Day 5（Sun） | 全天 | 官方课 Ch.4 + Actor 框架笔记 + 周报 | 6h |
| Day 6（Mon） | 晚间 | 蓝图变量与函数 | 2h |
| Day 7（Tue） | 晚间 | 蓝图事件与接口 | 2h |
| **合计** | | | **22h** |

---

## Day 1（今天）· 2 小时 · 环境与仓库

### 任务清单
- [ ] **0:00 - 0:10** 安装 Epic Games Launcher（[下载](https://store.epicgames.com/download)）
- [ ] **0:10 - 0:40** 通过 Epic Launcher 下载安装 UE 5.6（约 60GB，用零碎时间下，此刻先开始下载就行）
- [ ] **0:10 - 0:30** 下载 Visual Studio 2022 Community（[下载](https://visualstudio.microsoft.com/vs/community/)）
  - 安装时勾选：
    - `Game development with C++`（必选）
    - `Desktop development with C++`
    - 右侧单独组件勾 `Unreal Engine installer` 和 `Windows 10/11 SDK`
- [ ] **0:30 - 0:45** 注册 GitHub 账号（如果没有）+ 开启 2FA
- [ ] **0:45 - 1:00** Epic 账号绑定 GitHub
  - 访问 [https://www.unrealengine.com/en-US/ue-on-github](https://www.unrealengine.com/en-US/ue-on-github)
  - 登录 Epic → 输入 GitHub 用户名 → 同意 EULA
  - 去 GitHub 邮箱收邀请，点 Accept
  - 验证：访问 [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) 能打开即可
- [ ] **1:00 - 1:30** 配置本地 Git + 首次推送 `UE5-Journey` 仓库（见下方详细步骤）
- [ ] **1:30 - 2:00** 写 Day 1 日志（复制 `journal/TEMPLATE.md`）

### 把仓库推到 GitHub 的完整命令
打开 GitHub 网页，点右上角 `+` → `New repository` → 仓库名填 `UE5-Journey` → 选 `Public` → **不要勾** README / .gitignore / LICENSE（我们已经本地生成了）→ Create。

然后在 PowerShell 里依次跑（**把 YOUR_USERNAME 替换成你的 GitHub 用户名**）：

```powershell
# 设置 Git 身份（只需一次，用真实姓名和 GitHub 邮箱）
git config --global user.name "Your Name"
git config --global user.email "your_github_email@example.com"

# 推送到 GitHub（workspace 已经初始化为仓库）
cd d:\aaaWORK\Object\UE5
git remote add origin https://github.com/YOUR_USERNAME/UE5-Journey.git
git branch -M main
git push -u origin main

# 把 dev 分支也推上去
git push -u origin dev
```

---

## Day 2（Thu）· 2 小时 · Starter Course Ch.1

### 任务
- [ ] **0:00 - 1:30** 跟完 Epic 官方 [UE 5.7 Starter Course](https://dev.epicgames.com/community/learning/tutorials/bE7Z/unreal-engine-5-7-starter-course) 的 Chapter 1（Introduction & Installation）
  - 全程开英文字幕，不懂的词记到 `notes/english-vocabulary.md`
- [ ] **1:30 - 1:50** 在 `notes/ue5-concepts/` 建一个 `01-editor-basics.md`，记录今天的 3 个关键词（至少）
- [ ] **1:50 - 2:00** 写 Day 2 日志，commit + push

---

## Day 3（Fri）· 2 小时 · Starter Course Ch.2

### 任务
- [ ] **0:00 - 1:30** Starter Course Chapter 2（Navigating the Editor）
  - 重点练：Viewport 控制（鼠标中键/右键/F 聚焦）
  - 熟记快捷键：
    - `W/E/R` = 移动/旋转/缩放 Gizmo
    - `F` = 聚焦选中物体
    - `G` = 游戏视图切换
    - `Alt + 鼠标` = 环绕视角
- [ ] **1:30 - 1:50** 更新 `notes/ue5-concepts/01-editor-basics.md`
- [ ] **1:50 - 2:00** 日志 + commit

---

## Day 4（Sat）· 6 小时 · Starter Course Ch.3 + 第一个场景

### 任务
- [ ] **0:00 - 2:00** Starter Course Chapter 3（Actors & Placement）
- [ ] **2:00 - 2:30** 休息
- [ ] **2:30 - 5:00** 自己做一个"小岛场景"
  - 用 Quixel Megascans（通过 Fab）下载一些免费资源
  - 放 20 个以上 Actor（树、石头、建筑）
  - 加一个 Directional Light + Sky Atmosphere
  - 加一个 Player Start
  - 按 Play，用 WASD 走一圈
- [ ] **5:00 - 5:40** 录一段 10 秒 GIF（用 [ScreenToGif](https://www.screentogif.com/)），放进 `assets/`
- [ ] **5:40 - 6:00** 写 Day 4 日志，把 GIF 嵌进去

**关键：这是你第一次"做出来"东西，一定要录 GIF 发进仓库。**

---

## Day 5（Sun）· 6 小时 · Starter Course Ch.4 + 周报

### 任务
- [ ] **0:00 - 2:30** Starter Course Chapter 4（Blueprints Introduction）
  - 学：变量、Print String、Event BeginPlay、Tick
- [ ] **2:30 - 3:00** 休息
- [ ] **3:00 - 4:30** 练习：做一个"会闪烁颜色的方块"（用 Tick + Sine + Dynamic Material Instance）
- [ ] **4:30 - 5:30** 在 `notes/ue5-concepts/` 新建 `02-actor-framework.md`，画一张 UML 图（用 Excalidraw），梳理 Actor / Pawn / Character / Controller 的继承关系
- [ ] **5:30 - 6:00** 写 **Week 1 周报**（放 `journal/2026-04-xx-week-01-summary.md`），合并 dev 分支到 main：
  ```powershell
  git checkout main
  git merge dev
  git push origin main
  ```

---

## Day 6（Mon）· 2 小时 · 蓝图变量与函数

### 任务
- [ ] **0:00 - 1:30** 跟一个 YouTube 教程深入蓝图（推荐 Matt Aspland 的《Blueprint Basics》系列）
  - 重点：变量类型（Bool/Int/Float/String/Vector/Object）
  - 重点：自定义函数、函数参数、返回值
- [ ] **1:30 - 1:50** 笔记
- [ ] **1:50 - 2:00** 日志

---

## Day 7（Tue）· 2 小时 · 蓝图事件与接口

### 任务
- [ ] **0:00 - 1:30** 学：
  - Custom Event vs Function（区别：Event 可绑定 Dispatcher、Function 可返回值）
  - Event Dispatcher（事件分发器，对标 JS 的 EventEmitter）
  - Blueprint Interface（BPI，多态）
- [ ] **1:30 - 1:50** 笔记 + 画一个对比表（JS 对应 UE 概念）
- [ ] **1:50 - 2:00** 日志 + 规划第 2 周

---

## 每日结束检查表（复制粘贴到日志里）

```markdown
- [ ] 今天学的 3 个关键词（中英对照）记到 `notes/english-vocabulary.md`
- [ ] 新概念写进 `notes/ue5-concepts/`
- [ ] 至少 1 次 git commit
- [ ] 日志写完了
- [ ] 明天要做什么心里有数了
```

---

## 疑难问题怎么办

1. **装不上 UE**：Epic Launcher → Cache 清理 → 换安装路径（必须是英文路径，不能有空格中文）
2. **VS2022 没识别 UE 项目**：在 UE 里点 `Tools → Refresh Visual Studio Project`
3. **GitHub 慢**：用 [ghproxy.com](https://ghproxy.com) 代理，或开 Watt Toolkit
4. **蓝图崩溃**：UE 经常崩，随时保存（Ctrl+S），不要骂娘

---

**周日晚上写完周报后，把这份文件更新一下：下周学什么。**
