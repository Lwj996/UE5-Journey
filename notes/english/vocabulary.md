# UE5 英语词汇表

> 掌握这 50 个核心词，能读懂 80% 的 UE 官方文档。
> 每天增 1-3 个新词，配合 Anki 复习。

## 核心概念（必须背下）

| EN | 音标 | 中 | 场景 |
|----|------|-----|------|
| Actor | ˈæk.tɚ | 场景物体 | 所有 UE 文档 |
| Pawn | pɔːn | 可控制 Actor | 角色类型 |
| Character | ˈkær.ək.tɚ | 人形 Pawn | 玩家/NPC |
| Controller | kənˈtroʊ.lɚ | 控制器 | PlayerController/AIController |
| GameMode | ɡeɪm moʊd | 游戏模式 | 规则定义 |
| GameState | ɡeɪm steɪt | 游戏状态 | 全局可复制状态 |
| PlayerState | ˈpleɪ.ɚ steɪt | 玩家状态 | 玩家数据 |
| Component | kəmˈpoʊ.nənt | 组件 | Actor 的零件 |
| Blueprint | ˈbluː.prɪnt | 蓝图 | 可视化脚本 |
| Inheritance | ɪnˈher.ɪ.təns | 继承 | 类关系 |
| Instance | ˈɪn.stəns | 实例 | 对象化 |
| Spawn | spɔːn | 生成 | 创建 Actor |
| Destroy | dɪˈstrɔɪ | 销毁 | 移除 Actor |
| Cast | kæst | 类型转换 | 蓝图 Cast 节点 |
| Interface | ˈɪn.tɚ.feɪs | 接口 | BPI |
| Dispatcher | dɪˈspætʃ.ɚ | 分发器 | 事件分发 |
| Delegate | ˈdel.ə.ɡət | 委托 | C++ 事件 |

## 触发与生命周期

| EN | 中 |
|----|-----|
| Tick | 每帧调用 |
| BeginPlay | 开始运行时调用 |
| EndPlay | 结束时调用 |
| Event | 事件 |
| Trigger | 触发 |
| Callback | 回调 |

## 碰撞与物理

| EN | 中 |
|----|-----|
| Trace | 射线检测 |
| Collision | 碰撞 |
| Overlap | 重叠 |
| Hit | 命中 |
| Channel | 碰撞通道 |
| Response | 响应 |

## 联机

| EN | 中 |
|----|-----|
| Replication | 复制（联机同步） |
| RPC | 远程过程调用 |
| Authority | 权威端（Server） |
| Listen Server | 监听服务器 |
| Dedicated Server | 专用服务器 |

## 渲染

| EN | 中 |
|----|-----|
| Material | 材质 |
| Shader | 着色器 |
| Texture | 纹理 |
| Mesh | 网格 |
| Skeleton | 骨骼 |
| Animation | 动画 |
| Montage | 蒙太奇（动画片段） |
| Blend Space | 混合空间 |
| State Machine | 状态机 |
| Retargeting | 重定向（动画） |
| Rig | 绑定 |

## 现代 UE5 技术

| EN | 中 |
|----|-----|
| Lumen | 实时全局光照系统 |
| Nanite | 虚拟几何体系统 |
| Niagara | 粒子系统 |
| Sequencer | 过场动画编辑器 |
| MetaHuman | 数字人系统 |
| World Partition | 世界分区 |

## 开发与发布

| EN | 中 |
|----|-----|
| Packaging | 打包 |
| Cooking | 烘焙（资产预处理） |
| Shipping Build | 发布版本 |
| Debug Build | 调试版本 |
| Profiling | 性能分析 |
| LOD | 细节层次 |
| FPS | 每秒帧数 |
| Draw Call | 绘制调用 |
| Frustum Culling | 视锥剔除 |

---

## 简历高频词组

- `data-driven` — 数据驱动的
- `procedural generation` — 过程生成
- `optimization` — 优化
- `shipped` — 已发布（"I shipped a game" 比 "I made" 有力）
- `latency` — 延迟
- `throughput` — 吞吐量
- `memory footprint` — 内存占用
- `iteration` — 迭代
- `pipeline` — 管线 / 流程

## 面试常用表达

- "I implemented X using Y to achieve Z" — 我用 Y 实现了 X 达成 Z
- "I reduced X from A to B by doing Y" — 我通过 Y 把 X 从 A 降到 B
- "I'm familiar with / I have experience with" — 我熟悉 / 我有经验
- "Could you elaborate on..." — 你能详细说说...
- "Let me think for a moment" — 让我想一下（面试时可用，不要慌）

## Day 03 补录（2026-04-27）

| EN | 中 |
|----|-----|
| Developer Community (EDC) | Epic 开发者社区（发帖 / 搜答案） |
| Category / section | 分区（发帖选对类） |
| Project template | 工程模板（新建项目时选的那种） |
| Sample / starter content | 示例或入门内容包 |
| Repro steps | 复现步骤（提问要写清） |

---

**学习方法**：
1. 每天看英文教程时遇到生词，查了之后补到这里
2. 每晚睡前扫一眼
3. 周末用 Anki 集中复习
4. 3 个月后自然记住大部分
